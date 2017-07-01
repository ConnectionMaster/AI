# Artificial Intelligence Basics
The purpose of this program is to explore techniques in coding to build a basic artificial intelligence.  The goal is to study alternatives to advanced coding techniques.  Please note: This project is prototypical, so it is simplified, in the hopes of being useful for learning A.I. basics.  Learning advanced A.I. may take several years.


  #!/bin/bash

  HUMAN="I'M A HUMAN"
  REGEX="I'M A (.*)"
  TITLE="HUMAN: $HUMAN"
  
  if [[ $HUMAN =~ $REGEX ]]
  then
  RESPONSE="YOU'RE A ${BASH_REMATCH[1]}"
  fi

  F=$(printf "%-19s" "^")
  L="%s\n${F// /=^}\n\t"
  P="\n\t$L<-> <-> $L<o> <o> $L"

  printf "$P" "$TITLE" "$REGEX" "$RESPONSE"
  
  
  
