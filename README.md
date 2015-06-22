# basic_chatbot
The purpose of this program is to explore coding techniques in pure C++ to build a basic chat bot.  The goal is to study C++ alternatives to advanced coding techniques such as regular expressions.

	BASIC CHAT BOT IN C++

	YOU: hey
	 AI: HI THERE 

	YOU: ok
	 AI: TEACH ME [ OK ]


	YOU: no
	 AI: TRY NOT TO BE LIKE THAT 

	YOU: alright
	 AI: TEACH ME [ ALRIGHT ]


	YOU: bye
	 AI: PLEASE RETURN SOON
	 
------------------------------------------------------------------------------
/*   TITLE: Basic Chatbot is C++  ALPHA VERSION: 0.01
     AUTHOR: Tom Joyce COPYRIGHT. DATED: 6-22-2015  
     DESCRIPTION:  The purpose of this program is to explore
     coding techniques in pure C++ to build a basic chat bot.
     The goal is to study C++ alternatives to advanced coding 
     techniques such as regular expressions.

     COMPILES WITH: g++ basic_chat_bot.cpp -o basic_chat_bot.go
*/
#include<iostream>
#include<string>
#include<cstdlib>
#include<cstring>
#include<algorithm>

using namespace std;

string swap(string entered, string before, string after){
  size_t position = 0;
  while((position = entered.find(before, position)) != string::npos){
     entered.replace(position, before.length(), after);
     position += after.length();
  }
  return entered;
}

int found(string lookup, string text){
  if(text.find(lookup) != string::npos){
     return 1;
  }else{
     return 0;
  }
}
int main()
{
    string input;

    cout << endl << endl << "	BASIC CHAT BOT IN C++" << endl << endl;

    while(cin){
        cout << "	YOU: " ; getline(cin, input);

        for (int i = 0, len = input.size(); i < len; i++){
            if (ispunct(input[i])){
               input.erase(i--, 1);
               len = input.size();
               }
            }

        input = " "+input+" ";

        for(int i=0;input[i]!='\0';i++){
	    input[i]=toupper(input[i]);
           }

        input = swap(input, " I ", " i ");
        input = swap(input, " YOU ARE"," you are"); 
        input = swap(input, " AM "," am ");
        input = swap(input, " ME "," me ");
        input = swap(input, " YOU "," you ");
        input = swap(input, " MY "," my ");
        input = swap(input, " YOUR "," your "); 
        input = swap(input, " MINE "," mine ");
        input = swap(input, " ARE "," are ");
        input = swap(input, " me "," YOU ");
        input = swap(input, " my "," YOUR ");
        input = swap(input, " your "," AI "); 
        input = swap(input, " i "," YOU ");
        input = swap(input, " am "," ARE ");
        input = swap(input, " mine "," YOURS ");
        input = swap(input, " are "," IS ");
        input = swap(input, " you "," AI ");

        if (input.find(" HELLO ") != string::npos ||
            input.find(" HI ") != string::npos ||
            input.find(" HEY ") != string::npos){
           input = " HI THERE ";
	   }
        else if (input.find(" HOW IS AI ") != string::npos){
           input = " I AM BARELY ACCEPTABLE ";
	   }
        else if (found(" TEST ",input)){
           input = " TEST COMPLETE ";
	   }
        else if (input.find(" AI IS ") != string::npos){
           input = swap(input, " AI IS "," WHY DO YOU SAY I AM ");
	   }
        else if (input.find(" YOU ARE ") != string::npos){
           input = swap(input, " YOU ARE "," WHY DO YOU THINK YOU ARE ");
	   }
        else if (input.find(" YOU HAVE ") != string::npos){
           input = swap(input, " YOU HAVE "," HOW LONG HAVE YOU HAD ");
	   }
        else if (input.find(" YOU ") != string::npos){
           input = swap(input, " YOU "," WHEN DID YOU FIRST REALIZE THAT YOU ");
           }
        else if (input.find(" BECAUSE ") != string::npos){
           input = swap(input, " BECAUSE "," IS THAT REALLY THE REASON ")+"? ";
           }
        else if (input.find(" DO AI THINK ") != string::npos){
           input = swap(input, " DO AI THINK "," CAN YOU ANSWER THAT YOURSELF ")+"? ";
           }
        else if (input.find(" EAT ") != string::npos){   
           input = swap(input, " EAT "," NEED FOOD ")+"? ";;
           }
        else if (input.find(" YES ") != string::npos){
           input = swap(input, " YES "," HOW CAN YOU BE SURE ")+"? ";
           }
        else if (input.find(" NO ") != string::npos){
           input = swap(input, " NO "," TRY NOT TO BE LIKE THAT ");
           }
        else if (input.find(" WHO ")   != string::npos ||
                 input.find(" WHAT ")  != string::npos ||
                 input.find(" WHERE ") != string::npos ||
                 input.find(" WHEN ")  != string::npos ||
                 input.find(" WHY ")   != string::npos ||
                 input.find(" HOW ")   != string::npos 
                 ) {
           input = " GOOD QUESTION "; 
           }
        else if (input.find(" BYE ") != string::npos){
           cout << "	 AI: PLEASE RETURN SOON" << endl << endl << endl;
           exit(0);
           }
        else{input = " TEACH ME ["+input+"]\n";}

        input = input.substr(1);
        cout << "	 AI: " << input << endl << endl;
     };

return 0;
}


