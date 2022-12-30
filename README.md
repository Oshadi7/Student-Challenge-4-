import java.util.*;
import java.io.*;

class Student {
  private String firstName;
  private String lastName;
  private String course;
  private int finalExam;
  private double finalAverage;
  private char letterGrade;
  
  public Student(String firstName, String lastName, String course, int finalExam) {
    this.firstName = firstName;
    this.lastName = lastName;
    this.course = course;
    this.finalExam = finalExam;
  }
  
  public String getFirstName() { return firstName; }
  public String getLastName() { return lastName; }
  public String getCourse() { return course; }
  public int getFinalExam() { return finalExam; }
  public double getFinalAverage() { return finalAverage; }
  public char getLetterGrade() { return letterGrade; }
  
  public void setFinalAverage(double finalAverage) {
    this.finalAverage = finalAverage;
    if (finalAverage >= 90) letterGrade = 'A';
    else if (finalAverage >= 80) letterGrade = 'B';
    else if (finalAverage >= 70) letterGrade = 'C';
    else if (finalAverage >= 60) letterGrade = 'D';
    else letterGrade = 'F';
    
    class EnglishStudent extends Student {
   
  private int termPaper;
  private int midterm;
  
  public EnglishStudent(String firstName, String lastName, int termPaper, int midterm, int finalExam) {
    super(firstName, lastName, "English", finalExam);
    this.termPaper = termPaper;
    this.midterm = midterm;
    }
    
    public void computeFinalAverage() {
    double finalAverage = termPaper * 0.3 + midterm * 0.3 + finalExam * 0.4;
    setFinalAverage(finalAverage);
  }
}

class ScienceStudent extends Student {
  private int attendance;
  private int project;
  private int midterm;
  
   public ScienceStudent(String firstName, String lastName, int attendance, int project, int midterm, int finalExam) {
    super(firstName, lastName, "Science", finalExam);
    this.attendance = attendance;
    this.project = project;
    this.midterm = midterm;
  }

  public void computeFinalAverage() {
    double finalAverage = attendance * 0.1 + project * 0.3 + midterm * 0.3 + finalExam * 0.3;
    setFinalAverage(finalAverage);
  }
}


class MathStudent extends Student {
  private double quizAverage;
  private int test1;
  private int test2;

   public ScienceStudent(String firstName, String lastName, int attendance, int project, int midterm, int finalExam) {
    super(firstName, lastName, "Science", finalExam);
    this.attendance = attendance;
    this.project = project;
    this.midterm = midterm;
  }


  public void computeFinalAverage() {
    double finalAverage = attendance * 0.1 + project * 0.3 + midterm * 0.3 + finalExam * 0.3;
    setFinalAverage(finalAverage);
  }
}


class MathStudent extends Student {
  private double quizAverage;
  private int test1;
  private int test2;

 


