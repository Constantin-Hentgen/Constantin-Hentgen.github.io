---
title: Text-Parser
date: 2021-03-01 12:00:00 +0100
categories: [Personal project, Statistics]
tags: [python, languages, math]
pin: true
image:
  path: /book-page.webp
  alt: Responsive rendering of Chirpy theme on multiple devices.
---
# Typing Frequency Analysis Program

## Table of Contents

1. [Objective](#objective)
2. [Feedback](#feedback)
3. [Technologies Used](#technologies-used)
4. [Project Repository](#project-repository)
5. [License](#license)
6. [References](#references)

## Objective

Building on my initial experiences with typing, I developed a program to analyze the **frequencies of letters and characters** in various texts to generate an optimal keyboard configuration. This tool allows for the comparison of up to three text sources and produces a detailed PDF report.

> See article on the BÉPO layout: [BÉPO learning](https://constantin-hentgen.github.io/posts/Bepo-learning/)
{: .prompt-tip }

The program performs frequency analysis on characters common to the different sources, averages the results, and classifies them by language based on these averages. This analysis helps in designing keyboard layouts that balance typing loads between hands and prioritize faster, more powerful fingers over weaker ones.

The program calculates the frequency of character usage and visualizes the results, helping to position letters on the keyboard in a way that enhances typing efficiency. For example, the graph shows that the letter "e" is heavily used in German compared to French, which uses it less frequently. Additionally, the letter "h" is used less in French than in English and German, reflecting linguistic differences.

## Feedback

Developing this program has been both enjoyable and educational. It allowed me to explore the principles behind optimized keyboard layouts and provided a playful exploration of linguistic data. The project reinforced my programming skills and deepened my appreciation for the intersection of language and technology in improving typing efficiency.

## Technologies Used

### Python3

The main programming language used for data analysis and report generation.

- _Source:_ [Python Official Website](https://www.python.org/)

### Pandas

A library for data manipulation and analysis, used to process and analyze text data.

- _Source:_ [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)

### Matplotlib

A plotting library used to create visual representations of frequency data and comparisons.

- _Source:_ [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)

### ReportLab

A library for generating PDF documents from Python, used to produce the final reports.

- _Source:_ [ReportLab Documentation](https://www.reportlab.com/docs/reportlab-userguide.pdf)

## Project Repository

For more details on the implementation, access the source code, and explore the project, visit the GitHub repository:

- [Typing Frequency Analysis GitHub Repository](https://github.com/Constantin-Hentgen/Typing-Frequency-Analysis)

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/Constantin-Hentgen/Typing-Frequency-Analysis/blob/main/LICENSE) file for more information.

---

## References

- [Python Official Website](https://www.python.org/)
- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [ReportLab Documentation](https://www.reportlab.com/docs/reportlab-userguide.pdf)
- [Typing Frequency Analysis GitHub Repository](https://github.com/Constantin-Hentgen/Typing-Frequency-Analysis)
