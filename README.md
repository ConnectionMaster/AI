# Artificial Intelligence Basics
The purpose of this project is to explore coding techniques to build basic artificial intelligence.  The goal is to study how to get the most out of the basics as a possible alternative to advanced coding techniques.  A prototypical project may make it easier to learn fundamentals of A.I.  First we introduce pattern matching with wildcards called: Numbered Capturing Groups. "BASH_REMATCH[1]", stands for BASH Regular Expressions Match, captured and numbered one.


# SOURCE CODE

```bash
#!/bin/bash

human="I'M A HUMAN"
regex="I'M A (.*)"
title="HUMAN: $human"

if [[ $human =~ $regex ]]
then
response="YOU'RE A ${BASH_REMATCH[1]}"
fi

F=$(printf "%-19s" "^")
L="%s\n${F// /=^}\n\t"
P="\n\t$L<-> <-> $L<o> <o> $L"

printf "$P" "$title" "$regex" "$response"

  
```  
# PROGRAM OUTPUT

```
		YOU: I'M A HUMAN
	^=^=^=^=^=^=^=^=^=^=^=^=^=^=^=^=^=^=^
		<-> <-> I'M A (.*)
	^=^=^=^=^=^=^=^=^=^=^=^=^=^=^=^=^=^=^
		<o> <o> YOU'RE A HUMAN
	^=^=^=^=^=^=^=^=^=^=^=^=^=^=^=^=^=^=^
	


```
