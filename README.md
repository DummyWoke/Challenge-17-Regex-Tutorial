# Regex Tutorial

Welcome to my tutorial for Regex or "Regular Expressions" my goal is for you as a reader to develop a deeper understanding of this concept so that you yourself can find useful applications for this technology.

## Summary

Regular Expressions are a concept that can be incredibly useful for coding concepts while not inherently correlating to any programming language such as java script, python, C++, etc. While their appearance might seem incredibly intricate and complicated, they're incredibly useful for pattern recognition to search for similar data types.

This is achieved through the use of "meta characters" which are text characters with special meanings attached to them for the pattern recognition process.

An example of this is:

The meta character "\[(.+?)\]" which specifies the pattern being searched for as any character that is enclosed in a bracket. 

So in a string like "[Flowers] only [bloom] during [the] later months of spring."

the pattern will be recognized as searching for lines in brackets due to the regex character name being declared as \[(.+?)\]

Additionally you can combine multiple different regex character names together leading to an a more specified pattern to be recognized such as.

\[([A-Z]+?)\] ([[A-Z] is the meta character for uppercase letters) only selecting FLOWERS in the string of "[FLOWERS] only [bloom] during [the] later months of spring." due to it being the only text capitalized while being enclosed in brackets.

Any string can be recognized as a Regex pattern such as ("Globe Is A Toy")
From an initial viewing one can assume that there's is not pattern inside the string with seemingly random works, however using meta characters you can specify specific patterns such as "look for texts that are initially capitalized followed by lower case texts by using the meta character [a-z]. 


Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [Anchors](#anchors)

- [Quantifiers](#quantifiers)

- [OR Operator](#or-operator)

- [Character Classes](#character-classes)

- [Flags](#flags)

- [Grouping and Capturing](#grouping-and-capturing)

- [Bracket Expressions](#bracket-expressions)

- [Greedy and Lazy Match](#greedy-and-lazy-match)

- [Boundaries](#boundaries)

- [Back-references](#back-references)

- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors are used to search for a character either before after or even between a character.

    Example: "^" Searches for the character which appears at the front of the string, "$" Searches for the character at the end of the string.

    Further Example: "Yonkytodo" using ^ will select the Y while $ will select the o

    These characters can only be used to select either the start or end of a string.

### Quantifiers

Quantifiers are used to group character searches rather than execute a match for individual characters.

Example:"w*" would match all w texts in the string of "wdjiaswwksda", however rather than being two second selections, the "ww" text would be grouped together.

### OR Operator

The or operator let's the user register two possible modifiers as a selector

Example: "|" allows either the character Infront of it, or behind it to both be valid means of selection.

Used with a string ^(part1|part2)$ would select a string of either "part1"or"part2".

### Character Classes

Character classes allow for only specific characters in a set to be registered in selection.

Example: a class of "[AEW|Wow]" would only allow either "Wow" or "AEW" to be selected in a string of "AEW sadmadosakdsp[ad Wow".

### Flags

Flags provide a simple to use search criteria for the user

Example: Flags are represented by two backslashes, ("//")following the specific criteria the user wants to search for. "/ig/i" would select "ig IG" in a string of "ig IG sadasodpa" due to the flag specified being case insensitive.

### Grouping and Capturing

Capturing groups selects a specific declared set of characters and groups them depending on their location. They can additionally be assigned a number so they could be backreferenced and used in operations.

Example: (Pi){2} as a capture group would select "PiPiPiPi" and "Pi" from the string "PiPiPiPi sadpao Pi" additionally, this group would be accessible through the backreference of "2" due to the initial assignment of the character.

### Bracket Expressions

Expressions enclosed in square brackets declares that any text within the brackets will be selected (individually).

Example: [FnK] would select "F" and "n" "sidJadnadFASd" separately through the string. 

### Greedy and Lazy Match

Greedy and Lazy matches refer to the specifications of the selections made through meta characters.

An example of this is: within a string of "[sdasdsa]asdsadsad[AASD]", "\[(.+)\]" would select all content within the string of "[AEW sadma]dosakdsp[ad Wow]" due to it technically being between the two separate brackets, however a meta character selection of \[([A-Z]+?)\] would only select "[AASD]". In this instance using "\[(.+)\]" meta characters would be considered a greedy search.

### Boundaries

Boundaries allows for the user to select the entire word if one of the components are specified in the meta character.

For example: in a string of "Women of the world" a meta character specification of "\bO\b" would select the text of "Women, world, and of" due to them all containing the character of "o".

### Back-references

A back reference allows the user to assign a certain number to a capture group so that the user can easily reference the string selected.

Example: in a string of "Pi again" using the meta character of "(Pi){2}" will select characters containing "Pi" as well as assigning them with the number value of 2. this capture group can now be referenced by printing out "\2" to again reference the digit assigned.



### Look-ahead and Look-behind

Look behinds or look ahead start the execution of a selection based on if a certain object is either behind them or ahead of them.

Example: In a string of "wowow j kami j wowooww j nLiam" setting the meta character as (?(?<=kami)j|Liam) will set the selector to look for the text "kami" and look directly behind it for a character as indicated by the "?<=" since the condition of "j" being behind "kami" in the string the user will then select all text within the string which refer to "Liam"

## Author

This tutorial was created by Ramsey Banda

Link to the github repository aswell as finished page link.

https://github.com/DummyWoke/Challenge-5-Work-Day-Scheduler

https://dummywoke.github.io/Challenge-5-Work-Day-Scheduler/
