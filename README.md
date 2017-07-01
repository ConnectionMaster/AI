# Artificial Intelligence Basics
The purpose of this project is to explore coding techniques to build basic artificial intelligence.  The goal is to study how to get the most out of the basics as a possible alternative to advanced coding techniques.  As a prototypical project, it is simplified for learning A.I. fundamentals.  


# SOURCE CODE

```
#!/bin/bash

# DATA
human="I'M A HUMAN"
regex="I'M A (.*)"
title="YOU: $human"

# PROCESS
if [[ $human =~ $regex ]]
then
response="YOU'RE A ${BASH_REMATCH[1]}"
fi

# OUTPUT
F=$(printf "%-19s" "^")
L="%s\n${F// /=^}\n\t"
P="\n\t$L<-> <-> $L<o> <o> $L"

printf  "$title" "$regex" "$response"
  
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
