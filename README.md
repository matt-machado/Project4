# Project4
import java.util.Scanner;
import java.io.FileNotFoundException;
import java.io.File;
import java.util.ArrayList;
public static void main(String[] args){


/*
public class NameRecord { // encapsulates the data for one name; the name and its rank over the years. This is essentially the data of one line from the name_data.txt file.
   private int final START = 1900; // NameRecord constant START defines the start year of the data
   private int final DECADES = 11; // NameRecord constant DECADES defines the number of decades in the data
   Scanner t = new Scanner(System.in); // Scanner for user input of the name
   

    public void NameRecord() { // Constructor –takes a String line as in the file above and sets up the NameRecord object.
             ArrayList<String> listNames = new ArrayList<String>(); 
      ArrayList<ArrayList<Integer>> listRanks = new ArrayList<ArrayList<Integer>>(); // this is the ArrayList for all name's ranks. Each element is an Integer array of the ranks for one name.
 try (
   Scanner scanFile = new Scanner(new File("name_data.txt"));
 
   while (scanFile.hasNext()) {
     listNames.add(scanFile.next());
     ArrayList<Integer> ranks = new ArrayList<Integer>>(); // this is the array list for one name's ranks
        for (int i = 0; i < 11; ++i) {
             ranks.add(scanFile.nextInt());                  
         }
         listRanks.add(ranks);                      
   }
 )
   catch (Exception e) {
       e.printStackTrace();                        
                      }
    }

  public String getName() { // returns the name
      String target = t.next();
      return target;
  }
 
 public int getRank(int decade)  { // returns the rank of the name in the given decade. Use the convention that decade=0 is 1900, decade=1 is 1910, and so on. 
       int index = -1;
       String target = getName();
  for (int i = 0; i < listNames.size(); ++i) { // iterates through listNames to find the index of the name the user is looking for
      if (target.equals(listNames.get(i)) { // if the name is found in the ArrayList, return its index and don't keep looking
          index = i;
          break;
      } 
  }
  if (index < 0) { // index -1 means name is not found
     return -1; // 
  }
  else { // return the rank of the name in the given decade. 
     int rankRet = listRanks.get(index).get(decade); // decade is already provided from 0-11 range.
     return rankRet;                  
  }
  
  }
  public int bestYear() {
        int index = -1;
       String target = getName();
  for (int i = 0; i < listNames.size(); ++i) { // iterates through listNames to find the index of the name the user is looking for
      if (target.equals(listNames.get(i)) { // if the name is found in the ArrayList, return its index and don't keep looking
          index = i;
          break;
      } 
  }
  if (index < 0) { // index -1 means name is not found
     return -1; // 
  }
  else {
      int year = 0; 
      int min = 1100;
      for (int i = 0; i < listRanks.get(index).size(); ++i) {
           if (listRanks.get(index).get(i) != 0) {
               if (min > listRanks.get(index).get(i)) {
                   min = listRanks.get(index).get(i);
                   year = (i * 10) + (1900);
               } // if
           } // if
      } // for
    return year;
  }// else
   
 } // bestYear
  
} // class                            
*/



public static void main(String[] args) {
      ArrayList<String> listNames = new ArrayList<String>();
      ArrayList<ArrayList<Integer>> listRanks = new ArrayList<ArrayList<Integer>>();
 try {
   Scanner scanFile = new Scanner(new File("name_data.txt"));
 
   while (scanFile.hasNext()) {
     listNames.add(scanFile.next());
     ArrayList<Integer> ranks = new ArrayList<Integer>>();
        for (int i = 0; i < 11; ++i) {
             ranks.add(scanFile.nextInt());                  
         }
         listRanks.add(ranks);                      
   }
 
   } catch (Exception e) {
       e.printStackTrace();                        
                      }
   } 
                               
Scanner t = new Scanner(System.in);
String target = t.next();
int index = -1;
  
  
int j = 1;
int userInput;
  while (i > 0){ // FIXME- we need to add code for if the person does not enter 1,2,3,4, or 5
    System.out.println("1 - Find best year for a name");
    System.out.println("2 - Find best rank for a name"); // different from getRank(decade)
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
      // This would be the calling the bestYear()
      
   for (int i = 0; i < listNames.size(); ++i) {
      if (target.equals(listNames.get(i)) {
          index = i;
          break;
       } 
    }
  if (index < 0) {
     System.out.println("Cannot find the name");
    }
  else {
      int year = 0; 
      int min = 1100;
      for (int i = 0; i < listRanks.get(index).size(); ++i) {
           if (listRanks.get(index).get(i) != 0) {
               if (min > listRanks.get(index).get(i)) {
                   min = listRanks.get(index).get(i);
                   year = i;
               }
            }
           }
        System.out.println("best year = " + (1900 + (10 * year)));
      }
      
      
      break;

      case 2: //NOT getRank(). This is a different method.
      System.out.println("Write a name");
      userName = scan.next();
      
      // This would be calling bestRank() method, using the year/index to find the best rank???
      System.out.println("best rank = " + min);
      
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


/*
FOR CASE 2 BESTRank , not getRank
 int index = -1;
       String target = getName();
  for (int i = 0; i < listNames.size(); ++i) { // iterates through listNames to find the index of the name the user is looking for
      if (target.equals(listNames.get(i)) { // if the name is found in the ArrayList, return its index and don't keep looking
          index = i;
          break;
      } 
  }
  if (index < 0) { // index -1 means name is not found
     return -1; // 
  }
  else {
      int year = 0; 
      int min = 1100;
      for (int i = 0; i < listRanks.get(index).size(); ++i) {
           if (listRanks.get(index).get(i) != 0) {
               if (min > listRanks.get(index).get(i)) {
                   min = listRanks.get(index).get(i);
                   year = i;
               }
           }
      }
      System.out.println("best rank = " + min);
      System.out.println("best year = " + (1900 + (10 * year)));
  }


*/
