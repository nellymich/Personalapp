# Personalapp

package personalapp;
import javax.swing.*;

public class Personalapp {
    
    public static void main(String[] args) {
       
        JFrame myFrame = new JFrame("Q Offices");
        JPanel mypanel=new JPanel();
        JLabel namelabel = new JLabel("Username; ");
        JTextField name = new JTextField();
        name.setColumns(20);
        JButton submit = new JButton("Submit");
        mypanel.add(namelabel);       
        mypanel.add(submit);
        myFrame.add(mypanel);
        myFrame.setSize(500,400);
        myFrame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        myFrame.setVisible(true); 
    
    }
    
}
