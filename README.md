# Personalapp


package personalapp;
import java.awt.Component;
import java.awt.Event;
import java.awt.FlowLayout;
import java.awt.event.ActionListener;
import javax.swing.*;
import javax.swing.JRadioButton;//used in add_users
import javax.swing.ButtonGroup;
import static javafx.application.Application.launch;//used in piechart
import javafx.collections.FXCollections;
import javafx.collections.ObservableList;
import javafx.scene.Scene;
import javafx.stage.Stage;
import javafx.scene.chart.*;
import javafx.scene.Group;
import java.sql.*;

public class Personalapp_1 {

     //login 
    public static void main(String[] args) {
       
        JFrame myFrame = new JFrame("Q Offices");
        JPanel mypanel=new JPanel();
        JLabel namelabel = new JLabel("Username ");
        mypanel.add(namelabel);    
        JTextField name = new JTextField(20);
        mypanel.add(name);
        JLabel namelabel1=new JLabel("Password");
        mypanel.add(namelabel1);
        JPasswordField password = new JPasswordField(20);
        Component add = mypanel.add(password);
        JButton submit = new JButton("Submit");
        mypanel.add(submit);
        Component add1 = myFrame.add(mypanel);
       
        myFrame.setSize(300,400);
        myFrame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        myFrame.setVisible(true); 
    
    }
    JButton addActionListener = submit.addActionListener(new action);
    static action implements ActionListener{
    public void actionPerformed(Event Add_users){
        
        package personalapp;

//add_users
public class Add_users {
    public static void main(String[] args) {
       
        JFrame myFrame = new JFrame("Add User Form");
        JPanel mypanel=new JPanel();
        JLabel namelabel = new JLabel("First name ");
        mypanel.add(namelabel);    
        JTextField name = new JTextField(20);
        mypanel.add(name);
       
        JLabel namelabel0 = new JLabel("Last Name ");
        mypanel.add(namelabel0);    
        JTextField name0 = new JTextField(20);
        mypanel.add(name0);      
        JLabel namelabel1 = new JLabel("Telephone ");
        mypanel.add(namelabel1);    
        JTextField name1 = new JTextField(20);
        mypanel.add(name1);      
        JLabel namelabel2 = new JLabel("Date of Birth ");
        mypanel.add(namelabel2);    
        JTextField name2 = new JTextField(20);
        mypanel.add(name2);
        JLabel namelabel3 = new JLabel("Gender ");
        mypanel.add(namelabel3); 
        JRadioButton option1 = new JRadioButton("Male");
        JRadioButton option2 = new JRadioButton("Female");
        ButtonGroup group = new ButtonGroup();
        group.add(option1);
        group.add(option2);
        setLayout(new FlowLayout());
        add(option1);
        add(option2);
        pack();
        System.out.println(System.getProperty("line.separator"));
        JButton clear = new JButton("Clear");
        mypanel.add(clear);
        JButton save = new JButton("Save User");
        mypanel.add(save);
        myFrame.add(mypanel);
        myFrame.setSize(350,400);
        myFrame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        myFrame.setVisible(true);
}

    private static void add(JRadioButton option1) {
        throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
    }

    private static void setLayout(FlowLayout flowLayout) {
        throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
    }

    private static void pack() {
        throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
    }
}

//conecting database
public static void main (String[] args) {
    try {
        Class.forName("com.mysql.jdbc.Driver");
        Connection.con = DriverManager.getConnection("jdbc:derby://localhost:1527/sample [app on APP], "root", "");"
        System.out.println("Database Connected Successfully.")
    }catch(Eception e){
        System.out.println(e.getMessage());
    }
}
        
        
//columnchart
public class columnchart extends Personalapp_1 {
      public columnchart( String applicationTitle , String chartTitle ) {
      super( applicationTitle );        
      JFreeChart columnchart = ChartFactory.columnchart(
         chartTitle,           
         "Age",            
         "Number",            
         createDataset(),          
         PlotOrientation.VERTICAL,           
         true, true, false);
         
      ChartPanel chartPanel = new ChartPanel( columnchart );        
      chartPanel.setPreferredSize(new java.awt.Dimension( 560 , 367 ) );        
      setContentPane( chartPanel ); 
   }
   
   private CategoryDataset createDataset( ) {
      final int 0-18 = "0-18";        
      final int 18-25 = "18-25";        
      final int 26-30 = "26-30";        
      final int >30 = ">30";        
            
      final DefaultCategoryDataset dataset = 
      new DefaultCategoryDataset( );  

      dataset.addValue( 1.0 , 1-18);        
      dataset.addValue( 3.0 , 18-25);        
      dataset.addValue( 5.0 , 26-30); 
      dataset.addValue( 5.0 , >30);           
      return dataset; 
   }
   
   public static void main( String[ ] args ) {
      columnchart chart = new columnchart("Column Chart Showing Age Distribution");
      chart.pack( );        
      RefineryUtilities.centerFrameOnScreen( chart );        
      chart.setVisible( true ); 
   }
}
//piechart
public class piechart extends Personalapp {
    
    public void start(Stage stage) {
        Scene scene = new Scene(new Group());
        stage.setTitle("Chart showing Gender Distribution");
        stage.setWidth(250);
        stage.setHeight(250);
 
        ObservableList<PieChart.Data> pieChartData =
                FXCollections.observableArrayList(
                new PieChart.Data("Male", 13),
                new PieChart.Data("Female", 25));
        final PieChart chart = new PieChart(pieChartData);
        chart.setTitle("Chart showing Gender Distribution");

        ((Group) scene.getRoot()).getChildren().add(chart);
        stage.setScene(scene);
        stage.show();
    }
 
    public static void main(String[] args) {
        launch(args);
    }
}
    }
}
}
    

        
        
        

    

