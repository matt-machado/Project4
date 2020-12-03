# Project4
import java.util.Scanner;
import java.io.FileNotFoundException;
import java.io.File;
import java.util.ArrayList;
public static void main(String[] args){

try {
 ArrayList<String> nameList = new ArrayList<String>();
  File f = new File("name_data.txt");
  Scanner scan = new Scanner(f);

  int totalLines = 0;
  while(scan.hasNextLine()){
    scan.nextLine();
    totalLines++;
  }

  System.out.println(totalLines);

  scan = new Scanner(f);

  for (int i = 0; i < totalLines; i++) {
    while(scan.hasNextLine()){
      String name = scan.next();
      nameList.add(name);
      scan.nextLine();
  }
  }
 for (int i = 0; i < 1; i++){
   System.out.println(nameList.get(i));
 }



}catch(FileNotFoundException e) {
System.out.println(e.toString());
}
int i = 1;
int userInput;
  while (i > 0){
    System.out.println("1 - Find best year for a name");
    System.out.println("2 - Find best rank for a name");
    System.out.println("3 - Plot popularity of a name");
    System.out.println("4 - Clear plot");
    System.out.println("5 - Quit");
    System.out.println("Enter your selection.");
    userInput = scan.nextInt();
    String userName = "";
    switch (userInput) {
      case 1:
      System.out.println("Write a name");
      userName = scan.next();
      break;

      case 2:
      System.out.println("Write a name");
      userName = scan.next();
      
      break;

      case 3:
      System.out.println("Not implemented");
      break;

      case 4:
      System.out.println("Not implemented");
      break;

      case 5:
      i = -1;
      break;

      }
    }
  }
}


/*


public String getName() { // returns the name
 return ;
}

public int getRank(int getDecade) { // returns the rank of the name in the given decade. Use the convention that decade=0 is 1900, decade=1 is 1910, and so on. 




return ; // FIXME
}

public int bestYear() { /* –returns the year where the name was most popular, using the earliest year in the event of a tie. Looking at the data above Samir's best year is 2000, while Sandra's best year is 1940. Returns the actual year, for example 1920, so the caller does not need to adjust for START. It is safe to assume that no rank inthe data is ever larger than 1100, and every name has at least one year with a non-zero rank. */

int bestYear = 0; // best year would be 1900 by default
int maxRank = 0; // compare rankings
     
     }
    if ( > maxRank) {
      bestYear = (1900) + (10 * i);
    }
  }

return bestYear;
}

int final DECADES = 11; 

ArrayList<Integer[]> eachNameInfo = new ArrayList<Integer[]>;
Integer[] intNameRankings = new Integer[DECADES];
String[] oneNameRankings = new String[DECADES + 1]; // first string is the name, next are the rankings for each decade

for (i = 0; i < totalLines ; i++) { 
   String currentNameInfo = nameList.get(i);
   
                          
  for (j = 0; j < 11; ++j) { 
      int spaceLoc = currentNameInfo.indexOf(" ");
      if (j = 0) { // name
      int secondSpaceLoc = (currentNameInfo.substring((spaceLoc + 1),  currentNameInfo.length()).indexOf(" "); 
        oneNameRankings[j] = currentNameInfo.substring((spaceLoc + 1), (secondSpaceLoc)); 
      }
      else if (j < 11) { // string of numbers
      int secondSpaceLoc = (currentNameInfo.substring((spaceLoc + 1),  currentNameInfo.length()).indexOf(" "); 
        oneNameRankings[j] = currentNameInfo.substring((spaceLoc + 1), (secondSpaceLoc));  
        
       }
      else if (j == 11) { // last number, has no last space.(i think?)
        oneNameRankings[j] = currentNameInfo.substring((spaceLoc + 1), (currentNameInfo.length() + 1));            
      }
   
   if (j > 0) {
      intNameRankings[j] = oneNameRankings[j].toInteger();
   }
  } // for j
  
 eachNameInfo[i] = intNameRankings; /// can scan for the name, use the line number as the [i] to find the ranks. use the decade 1-11 to access which element of intNameRankings needed
  
 } // for i

*/
