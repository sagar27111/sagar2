import java.util.Scanner;

class Result
{

public static void main(String arg[])
{
    String name, USN;   
    int i, Gtotal=0,count=0;
    float percentage;
 String subject[] = { "MANAGEMENT AND ECONOMICS", "DESING OF MACHINE ELEMETS 1", "DYNAMICS OF MACHINE","FLUID POWER ENGINEERING","TURBO MACHINES","OPERATION MANAGEMENT","FLUID MECHANICS/MACHINES LAB","ENERGY CONVERSION LAB","ENVIRONMENT STUDIES"}; String subcode[]= { "18ME51","18ME52","18ME53","18ME54","18ME55","18ME56","18ME57","18ME58","18CV59"};
 int iamarks[]= new int[9];
 int semmarks[]= new int[9];
  Scanner s = new Scanner(System.in);
  System.out.println("\t Enter your Full Name:");
  name = s.nextLine();
  System.out.println("\t Enter your USN:");
  USN = s.nextLine();
for(i=0;i<9;i++)
{
    System.out.println("\t Enter IA Marks for: "+subject[i]+":");
    iamarks[i] = s.nextInt();
}
 System.out.println("\n\t\t\tOK NOW ENTER EXTERNALS");
for(i=0;i<9;i++)
{
    System.out.println("\t Enter Final Exam Marks for: "+subject[i]+":");
    semmarks[i] = s.nextInt();
}

  System.out.println("\t\t\t\t\tYOUR RESULT\n");
  System.out.println("\t\t**VISVESVARAYAN TECHNOLOGICAL UNIVERSITY**\n");
  System.out.println("\t\t College:\t"+"Ballari Institute Of Technology And Management\n");
  System.out.print("\n\t\t Name:" +name);
  System.out.println("\t\t USN:"+USN);
  System.out.println("\n\t\t "+"Subcode"+"\tIA"+"\tEXA"+"\tTotal");

for(i=0;i<9;i++)
{
       if(((iamarks[i])+(semmarks[i])) >=40)
       {
        System.out.println("\t\t "+subcode[i]+"\t\t "+iamarks[i]+"\t"+semmarks[i]+"\t"+((iamarks[i])+(semmarks[i])));
       }
       else
      {
      System.out.println("\t\t "+subcode[i]+"\t\t "+iamarks[i]+"\t"+semmarks[i]+"\t"+((iamarks[i])+(semmarks[i]))+"*");
      count++;
      }
      Gtotal = (Gtotal + ((iamarks[i])+(semmarks[i])));
}
if(count >0)
{
 System.out.println("\n\t\t Grand Total:\t"+Gtotal+"\tResult: \tFAIL");
}
else
{
System.out.println("\n\t\t Grand Total:\t"+Gtotal+"\tResult:\tPASS");
}
{
	 percentage = (Gtotal /9);
     System.out.println(
         "\t\tTotal Percentage : " + percentage + "%");
}
}
}
