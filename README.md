# Ternary-operatorJava-Assignment
#  create a java code for travel capablity of a person under a certain conditions;

import java.util.Scanner;

public class TravelCapablity{
    public static void main(String[] args) {
       
        System.out.println("****** Please Enter your Status as follow ********** ");

        System.out.println(" \n Any criminal record? True/False");
        Scanner in = new Scanner(System.in);
        boolean criminalRecord = in.nextBoolean();
         System.out.println("****** **** **********" );
        System.out.println("\n Enter monthly bank saving amount : ");
        int bankSavingAmount= in.nextInt();
        int perYearBankSaving = bankSavingAmount * 12;
        System.out.println("Your yearly saving amount is :"+ perYearBankSaving);
        System.out.println("******** **** **********");
        System.out.println("\n Enter monthly salary: ");
        int Salary = in.nextInt();
        
        int perYearSalary = Salary * 12;
        System.out.println("Your yearly Salary amount is :"+ perYearSalary);
        System.out.println("******* **** **********  ");
        System.out.println("\n Number of faults per Month:");
        int SocialScore = in.nextInt();
        int numberFault = SocialScore * 12;
         System.out.println("\n Your yearly SocialScore amount is :"+ numberFault);
         System.out.println("******* **** **********");
        String Travel = !criminalRecord && (perYearBankSaving>6_000_000 )&& (perYearSalary > 70_000) && (numberFault<50)?"Congratulation! You can travel any where.":"You cann't travel.";
        System.out.println("Hello Mr. : " +Travel);
    }
}
