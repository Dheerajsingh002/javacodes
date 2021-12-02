import java.sql.*;
import java.util.Objects;
import java.util.Scanner;

public class StudentInfo{

    Connection con = DriverManager.getConnection("jdbc:mysql://localhost:3306/jdbc", "root", "123456");
    Statement s = con.createStatement();


    public StudentInfo() throws SQLException, ClassNotFoundException {
        Class.forName("com.mysql.cj.jdbc.Driver");
    }

    public void create(String contact_no,String First_Name, String Last_Name, String DOB, String Age, String College, String section, String Branch) throws SQLException {

        String query = "INSERT INTO data VALUES(?,?,?,?,?,?,?,?)";

        PreparedStatement smt = con.prepareStatement(query);
        smt.setString(1,contact_no);
        smt.setString(2,First_Name);
        smt.setString(3,Last_Name);
        smt.setString(4,DOB);
        smt.setString(5,Age);
        smt.setString(6,College);
        smt.setString(7,section);
        smt.setString(8,Branch);

        smt.execute();


    }
    public void Read(String Contact) throws SQLException {



            String query = "SELECT * FROM data WHERE Contact_Number=?";

            PreparedStatement smt = con.prepareStatement(query);

            smt.setString(1, Contact);

            ResultSet rs = smt.executeQuery();
            String check = "";

                while (rs.next()) {
                    System.out.println(rs.getString("First_Name"));

                    check = rs.getString("First_Name");

                    System.out.println(rs.getString("Last_Name"));
                    System.out.println(rs.getString("DOB"));
                    System.out.println(rs.getString("Age"));
                    System.out.println(rs.getString("University"));
                    System.out.println(rs.getString("Section"));
                    System.out.println(rs.getString("Branch"));
                    System.out.println(rs.getString("Contact_Number"));
                }
                if(check.equals("")){
                    System.out.println("Student's information not found!");
                }
    }
    public void Update(String column,String place,String value)  {

        try {
           if(place=="First_Name") {

               String query2 = "UPDATE data SET First_Name=? WHERE Contact_Number=?";
               PreparedStatement smt = con.prepareStatement(query2);
               smt.setString(1, value);
               smt.setString(2, column);
               smt.execute();

           }
            else if(place=="Last_Name") {

                String query2 = "UPDATE data SET Last_Name=? WHERE Contact_Number=?";
                PreparedStatement smt = con.prepareStatement(query2);
                smt.setString(1, value);
                smt.setString(2, column);
                smt.execute();

            }
            else if(place=="DOB") {

                String query2 = "UPDATE data SET DOB=? WHERE Contact_Number=?";
                PreparedStatement smt = con.prepareStatement(query2);
                smt.setString(1, value);
                smt.setString(2, column);
                smt.execute();

            }
            else if(place=="Age") {

                String query2 = "UPDATE data SET Age=? WHERE Contact_Number=?";
                PreparedStatement smt = con.prepareStatement(query2);
                smt.setString(1, value);
                smt.setString(2, column);
                smt.execute();

            }
            else if(place=="University") {

                String query2 = "UPDATE data SET University=? WHERE Contact_Number=?";
                PreparedStatement smt = con.prepareStatement(query2);
                smt.setString(1, value);
                smt.setString(2, column);
                smt.execute();

            }
            else if(place=="Section") {

                String query2 = "UPDATE data SET Section=? WHERE Contact_Number=?";
                PreparedStatement smt = con.prepareStatement(query2);
                smt.setString(1, value);
                smt.setString(2, column);
                smt.execute();

            }
            else if(place=="Branch") {

                String query2 = "UPDATE data SET Branch=? WHERE Contact_Number=?";
                PreparedStatement smt = con.prepareStatement(query2);
                smt.setString(1, value);
                smt.setString(2, column);
                smt.execute();

            }
            System.out.println("Data updated successfully!");

        }
        catch(SQLException e){
            System.out.println("Student not found!");
        }
    }
    public void Delete(String Contact){
        try {

            String query3 = "DELETE FROM data WHERE Contact_Number=?";
            PreparedStatement smt = con.prepareStatement(query3);
            smt.setString(1,Contact);
            smt.execute();

            System.out.println("Record deleted successfully!");
        }
        catch(SQLException e){

            System.out.println("Student not found!");

        }
    }

    public static void main(String[] args) throws SQLException, ClassNotFoundException {


        StudentInfo obj = new StudentInfo();
        Scanner sc = new Scanner(System.in);

        System.out.println("do you want to enter details of new student?:");
        String ans = sc.nextLine();
        System.out.println("Do ou want to read the studentInfo?:");
        String ans1 = sc.nextLine();
        System.out.println("Do ou want to update the studentInfo?:");
        String ans2 = sc.nextLine();
        System.out.println("Do ou want to delete the studentInfo?:");
        String ans3 = sc.nextLine();

       if(ans.equals("yes")) {

            System.out.println("Enter the details:");
            String Contact2 = sc.next();
            String First_Name = sc.next();
            String Last_Name = sc.next();
            String DOB = sc.next();
            String Age = sc.next();
            String University = sc.next();
            String Section = sc.next();
            String Branch = sc.next();

            obj.create(Contact2,First_Name,Last_Name,DOB,Age,University,Section,Branch);
        }

       if(ans1.equals("yes")){
           System.out.println("specify the studentInfo:");
           String Contact = sc.next();
           obj.Read(Contact);

       }

       if(ans2.equals("yes")){
           System.out.println("enter the table_name,place,value:");
           String table_name = sc.nextLine();
           String place = sc.nextLine();
           String value = sc.nextLine();
           obj.Update(table_name,place,value);

       }

       if(ans3.equals("yes")){
           System.out.println("enter the table name to delete:");
           String Contact1 = sc.next();
           obj.Delete(Contact1);

       }
    }
}
