---
layout: post
title: "Ideas for a magic mod/system"
date: 2021-07-09 12:41:00 -0000
tags: [Minecraft, Modding]
---

# Design Ideas for a magic mod based on formal languages

## Abstract
This document gathers preliminary ideas for the design of a magic themed minecraft mod where spells are well formed sentences from a formal language whose rules are randomly generated for each world. The objective is to offer an entirely new experience with each playthrough by introducing a lot of variation in the possible rules. The effect of spells is not hardcoded, rather, the spells that can be expressed in a given language are entirely determined by its rules.


## Overall Goals
* The experience of progressing through the mod should be radically different for each playthrough.
* The rules of a given language are never given explicitly. Players must discover them by experimenting, and possibly with hints in the form of dungeon loot.
* The mod should be highly modular and allow in-depth configuration of how languages are generated.
* The variety of languages should be finely tuned to avoid being unbearably tedious.
General Design Principles
* At high level, languages may allow for game breaking spells, but this should be balanced by constraints.
* Information about the magic system should be hidden or obfuscated by default. For instance, if the language has a form of “mana”, the current amount and total capacity of this resource should not be given explicitly to the player from the start. Rather, spells, or items can be later devised to provide that information. That being said, properly communicating to the player at every stage of the mod is very important.
* As little as possible is hardcoded.
* Players are encouraged to share their knowledge with each other?
Formal languages
The core of the mod consists of formal languages whose rules are generated randomly. In particular, we intend to use ideas from the field of sequent calculus and non-classical logic Examples of non-classical logics include
* Intuitionist logic, which rejects the law of excluded middle
* Paraconsistent logics (logics that allow the presence of contradiction by restraining the “explosion of truth” problem)
* Many-valued logics, which introduce other truth values than True and False. Intuitionistic logic is one such system.
* Linear logic, which can be thought of the logic of consumable resources (this is the natural language for crafting systems in video games such as minecraft, but also for parallel programming and quantum computing)
* Fuzzy logic and Probabilistic logic, in which the truth value of a given proposition is is real number in the interval [0,1] (These two systems differ in what the truth value means. Fuzzy logic is the logic of vagueness, while Probabilistic logic is the logic of uncertainty)
* Modal logic, which is concerned with formalizing propositions being possibly or necessarily true.
* Categorial Grammars/ Noncommutative Logic
* ...
Not all of these are practical for this mod. For example, the typical language of Modal logic, given by Kripke, concerns itself with multiple “worlds” in which a proposition may be true or false. It is unclear how to translate that into game mechanics in a practical way.


Since we want spells to be “theorems” of our randomly generated languages, these languages need to be relatively weak, both for game balance and for performance.


## Syntaxes
While the underlying rules of the magic system are described by formal languages, another layer of interaction lies in the “syntax” in which spells are expressed. In this regard, we need not restrict ourselves to strings of symbols. Many interesting examples can be found among esoteric programming languages, such as Piet. Possible syntaxes include
* Flower beds: Spells are made by arranging flowers in specific patterns. Rules may include that the patterns be a certain shape, follow a certain symmetry, ....
* Cooking recipes: Spells are made by preparing food with specific ingredients in a specific order.
* Poetry: Spells are strings of symbols that follow some form of “poetic” constraints (e.g. written in verse, must be of a certain length). This allows for interesting mechanics, such as spells being more potent the more rules they follow/how well they follow them. This is a broad category, as there are many rules imaginable. (See esolangs like Shakespeare for examples)
* Ideograms: Symbols directly represent objects, such as in Eastern languages like Chinese. This also includes “atypical” (for the average western player) sentence structures. (Note: we can use the magical symbols from minecraft for this)
The interesting thing about these is that they naturally influence the “metagame” around which spells are actually used. For instance, spells in the flower bed syntax take time to “write”, so that syntax favours more passive/long term spells to be used.