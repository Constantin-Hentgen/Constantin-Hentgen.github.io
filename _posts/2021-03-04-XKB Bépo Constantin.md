---
title: XKB Bépo Constantin
date: 2021-03-04 12:00:00 +0100
categories: [Personal project, Setup]
tags: [linux, keyboard layout]
pin: false
image:
  path: /debian.webp
  alt: A computer screen displaying a debian configuration.
---
# xkb_fr-BÉPO

> See my Github repository: [XKB-bepo-constantin](https://github.com/Constantin-Hentgen/XKB-bepo-constantin)
{: .prompt-tip}

## Table of Contents

1. [What is "xkb"?](#what-is-xkb)
2. [What is the purpose of this repository?](#what-is-the-purpose-of-this-repository)
3. [What's the matter basically?](#whats-the-matter-basically)
4. [What if I want to try it out?](#what-if-i-want-to-try-it-out)
5. [Boring stuff](#boring-stuff)

---

## What is "xkb"?

xkb file is a directory under Linux-based distributions that rules the keymaps. This means that the logic behind the keys pushed is saved in this directory and allows us to customize our keyboard layouts.

The path to reach these documents is the following:
```
/usr/share/X11/xkb/symbols/
```

---

## What is the purpose of this repository?

Here is an archive of my keyboard's layout that allows me to find it wherever I am and also allows the community to maybe get inspired by it.

---

## What's the matter basically?

It's a custom BÉPO layout improved for coding and fast typing.
BÉPO is basically a French adaptation of the Dvorak layout which has been made for English Dactylography.

The points I touched upon in order to carry out that:

1. Avoiding the dead keys
2. Bringing brackets right under the right hand's fingers
3. Binding slashes on the space bar in order to make navigation easier


|Here is the keymap of my BÉPO version|
|-|
|![bepo layout](/bepo.webp)|

> For more details and to download the layout, visit the [GitHub repository](https://github.com/Constantin-Hentgen/XKB-bepo-constantin).
{: .prompt-tip }

---

## What if I want to try it out?

_Read **entirely** the README if you really want to try it out: probable issues identified at the end._

1. The only way possible is to copy my code and then paste it instead of the previous statement called:

```
default partial alphanumeric_keys
xkb_symbols "basic" {
```
2. When it's done, make sure you added the correct keyboard layout with `Gnome Settings` or `ibus`.
- _Tips: I advise you to keep your previous layout **INTACT** and just edit another one in case an issue arises._
3. Then you can logout or reboot to refresh the session.
4. Toggle to your new keyboard by selecting it in the GUI used by your system or by using the shortcut `meta + space`.

---


> I'm not responsible for any issue caused while following this tutorial: this is a suggestion of help to use it, that's all (though I struggle to imagine how a problem could occur here…)
{: .prompt-warning }

> There are two worst cases you could face:
  1. You have only one keyboard layout set up on your system which is not equal to the layout printed on your physical keyboard (or you have a blank keyboard). You _badly_ rewrote the file that rules this layout (making the layout nonfunctional). You logout and you don't succeed to login because the system is using `default QWERTY us`.
  2. You have only one keyboard layout set up on your system which is not equal to the layout printed on your physical keyboard (or you have a blank keyboard). You _correctly_ rewrote the file that rules this layout BUT you forgot a character that you need for your session password. You logout and you don't succeed to login.
{: .prompt-danger }

