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
