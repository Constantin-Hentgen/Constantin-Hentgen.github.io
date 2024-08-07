---
title: Citadelles
date: 2021-11-15 12:00:00 +0100
categories: [App, Game]
tags: [java, game]
render_with_liquid: false
image:
  path: /board-game.webp
  lqip: data:image/webp;base64,UklGRuoBAABXRUJQVlA4IN4BAADQCQCdASoyACEAPp1CnUqlo6KhqrQLALATiWUAx40vScemAQK6ELOhQM/Ah837hmqvvuA4Q4LwFCVmOQoo2J3Am8vN7hFJQtygFoxq6y1lW+nSQcPxThgA/v2uY2tA78NPN1uZzavqdPWS8ZluepEc8PmNEPxAa7IKIjGq0w/jpZF2xQHkscBFE0sKuLsEcMGqvg+QBPDnKmIC650g2qY8zSl/FOiSTgKSviBazcluwK5k1Ct9eC2usqhOUsByeiLVFtBhDQTXtO990xTo6rAxuPJvwxtnyBv8rpZkaDbouE7xO8sIZbw/osPf8+x4GWQeZc7wMwDIAt8637Ko1qXft2rL5Q8ypSLf/8Fybv2ek9RiTFuMuVVJrqr4/QJfwQxQKc2/eYpF5HcSGA+M907hpXZHnSnxhjbXlpt/h5heVvyhUcTH8JG/ZZ5SnekB8wPQxJU/X8VcsnvOADlDwjANuFha7SBw6ZC/whV8SUhXNJNMkusG3ge/vzyA2xBs0fSVoGqfU5jaLb8wUIdDb8ZloCyDaOd9uk8qa0qCrLhh4+0hyGz9AMUQlkS8Bx3DfASPqH7r7jKJpGfRPBHeZO2yK4Gia5h69ZgQ6TCkkuA/aIgY0GbejjIxOZEg0AAA
  alt: A board game.
---

As part of the Object-Oriented Programming (OOP) course at ESAIP, a school of engineering, I worked with a team to develop Citadelles, a digital version of a popular board game. This project allowed us to apply our OOP skills in a collaborative environment. The team comprised Constantin Hentgen, Mathieu Guignard, Alan Grillo, and Rémi Guérin. Here, I share our development journey, the challenges we faced, and the resources that aided us along the way.

# Table of Contents

1. [Project Overview](#project-overview)
2. [Learning and Applying Object-Oriented Programming](#learning-and-applying-object-oriented-programming)
   - [Why Object-Oriented Programming?](#why-object-oriented-programming)
   - [Resources for Learning OOP](#resources-for-learning-oop)
3. [Development Process](#development-process)
   - [Initial Setup](#initial-setup)
   - [Designing the Game](#designing-the-game)
     - [Class Diagrams](#class-diagrams)
     - [Core Classes](#core-classes)
4. [Challenges and Solutions](#challenges-and-solutions)
   - [Team Collaboration](#team-collaboration)
   - [Implementing Game Rules](#implementing-game-rules)
   - [User Interface Design](#user-interface-design)
5. [Conclusion](#conclusion)
6. [References](#references)

# Project Overview

Citadelles is a digital adaptation of the Citadelles board game, implemented using object-oriented programming principles. The project involved designing and coding various game components, such as characters, districts, and game logic, to create a functional and engaging game experience.

# Learning and Applying Object-Oriented Programming

## Why Object-Oriented Programming?

Object-oriented programming is a paradigm that uses objects and classes to structure software. It promotes code reuse, modularity, and scalability, making it ideal for complex applications like games.

## Resources for Learning OOP

- **OOP Principles:** Understanding the four main principles of OOP—encapsulation, inheritance, polymorphism, and abstraction—was crucial. [GeeksforGeeks](https://www.geeksforgeeks.org/object-oriented-programming-oops-concept-in-java/) offers a comprehensive guide on these concepts.
- **Design Patterns:** We referred to the book _Design Patterns: Elements of Reusable Object-Oriented Software_ by Erich Gamma, Richard Helm, Ralph Johnson, and John Vlissides to understand common solutions to recurring design problems.
- **Online Tutorials:** Websites like [Coursera](https://www.coursera.org/) and [Udemy](https://www.udemy.com/) provided courses on OOP and game development.

# Development Process

## Initial Setup

We started by setting up a shared repository on GitHub for version control and collaboration. This ensured that all team members could contribute and track changes efficiently.

## Designing the Game

### Class Diagrams

Creating class diagrams helped us visualize the structure of the game and the relationships between different components. Key classes included `Game`, `Player`, `Character`, `District`, and `Deck`.

### Core Classes

Here is an example of how we defined one of the type of characters, the `Roi` class:

```java
package modele;

public class Roi extends Personnage {
	public Roi() {
		super("Roi",Caracteristiques.ROI,4);
	}

	public void percevoirRessourcesSpecifiques() {
		int compteur = 0;
		if (this.joueur != null && this.assassine != true) {
			for (Quartier unQuartier : joueur.getCite()) {
				if (unQuartier != null && unQuartier.getType() == "NOBLE") {
					compteur ++;
				}
			}
			this.joueur.ajouterPieces(compteur);
		}
	}

	public void utiliserPouvoir() {
		if (this.joueur != null && this.assassine != true) {
			System.out.println("\n\tLe joueur prend la couronne.");

			for (int i = 0; i < this.plateau.getNombreJoueurs(); i++) {
				this.plateau.getJoueur(i).setPossedeCouronne(false);
			}

			joueur.setPossedeCouronne(true);
		}
	}

	public void utiliserPouvoirAvatar() {
		if (this.joueur != null && this.assassine != true) {
			System.out.println("\n\tLe joueur prend la couronne.");

			for (int i = 0; i < this.plateau.getNombreJoueurs(); i++) {
				this.plateau.getJoueur(i).setPossedeCouronne(false);
			}

			joueur.setPossedeCouronne(true);
		}
	}
}
```

Here’s a snippet demonstrating a test for the Roi character:

```java
ppublic void test7(){
		System.out.println("TEST DE LA CONSTRUCTION D'UN QUARTIER DANS LA CITE DU JOUEUR");
		Quartier quartier1 = new Quartier("temple",Quartier.TYPE_QUARTIERS[0],1);
		Quartier quartier2 = new Quartier("prison",Quartier.TYPE_QUARTIERS[1],2);
		Quartier quartier3 = new Quartier("palais",Quartier.TYPE_QUARTIERS[2],5);
		Joueur joueur = new Joueur("Billy");
		Roi roi = new Roi();
		roi.construire(quartier1);
		Test.test(roi.getJoueur() == null,
				"test alors que le joueur n'est pas attribué");
		roi.setJoueur(joueur);
		roi.construire(quartier1);
		roi.construire(quartier2);
		roi.construire(quartier3);
		Test.test(roi.getJoueur().nbQuartiersDansCite() == 3,
				"test du nombre de quartiers après construction");
		Test.test(roi.getJoueur().quartierPresentDansCite("prison"),
				"test de la présence de la prison dans la cité");
	}
```

# Challenges and Solutions

## Team Collaboration
Coordinating work among team members was challenging. We used GitHub issues and pull requests to manage tasks and code reviews, ensuring consistent code quality and integration.

## Implementing Game Rules

Translating complex game rules into code required careful planning and testing. We wrote unit tests for each game component to ensure correctness and robustness.

## User Interface Design

Creating an intuitive and appealing user interface was crucial for player engagement. We iterated on the design based on feedback from peers and test users, improving usability and aesthetics.

# Conclusion

Developing Citadelles was a rewarding experience that enhanced our understanding of object-oriented programming and teamwork. We successfully created a functional and enjoyable game, showcasing our ability to apply OOP principles in a real-world project. I encourage anyone interested in OOP or game development to check out the project on [GitHub](https://github.com/Constantin-Hentgen/Citadelles).

---

# References

- https://github.com/Constantin-Hentgen/Citadelles
