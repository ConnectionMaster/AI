# Artificial Intelligence Basics
The purpose of this article is to explore coding techniques to build a basic artificial intelligence.  The goal is to study how to get the most out of A.I. basic as a possible alternative to advanced coding techniques.  This project is prototypical, so it is simplified, for learning A.I. basics.  


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
