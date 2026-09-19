# PROG5121-ICE-Task-5
ICE Task 5
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 */

package com.mycompany.prog5121_icetask5;

/**
 *
 * @author sethu
 */
public class PROG5121_ICETASK5 {

    public static void main(String[] args) {
       
        //Declare the index
        final int numOfStudents = 5;
        
        //Parallel array: names and test scores
        String[] studentName = {"Selena", "Lerato", "Tshepo", "Sethu", "Lesedi"};
        int[] testScore = {55, 90, 77, 65, 80};
        
        //Bubble sort the test scores from highest to lowest
        int a, b;
        int tempTestScore;
        String tempStudentName;
        
        for(a = 0; a < numOfStudents - 1; ++a){
            for(b = 0; b < numOfStudents - 1; ++b){
                if(testScore[b] < testScore[b + 1]){
                
                    //Swap the testScores
                    tempTestScore = testScore[b];
                    testScore[b] = testScore[b + 1];
                    testScore[b + 1] = tempTestScore;
                    
                    //Swap the student names
                    tempStudentName = studentName[b];
                    studentName[b] = studentName[b + 1];
                    studentName[b + 1] = tempStudentName;                                                
                }
            }
        }
        
        //Display the student names and scores from highlest to lowest
        System.out.println("Sorted student names and scores:");
        display(studentName, testScore);
    }
    
    public static void display(String[] names, int[] scores){
      for(int x = 0; x < names.length; ++x)
         System.out.println(names[x] + "\t" + scores[x]);
    }
}
