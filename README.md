import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class FoodOrderingSystem extends JFrame implements ActionListener{
    JLabel textHeader, Description;
    JCheckBox riceBeans, chapati, tea, chips, stew, mandazi;
    JButton b;
    FoodOrderingSystem(){
        textHeader = new JLabel("SOKO HOTEL MENU");
        textHeader.setBounds(50, 50, 500, 30);
        textHeader.setBackground(Color.BLUE);
        textHeader.setFont(new Font("Times New Roman", Font.PLAIN, 35));

        Description = new JLabel();
        Description.setText("P.O BOX XXXX Hotline: 07xxxxxxxx  KARIBU TENA");
        Description.setBounds(20, 500, 500, 30);
        Description.setBackground(Color.BLUE);
        Description.setFont(new Font("Times New Roman", Font.PLAIN, 15));

        riceBeans = new JCheckBox("Rice & Beans @ 60");
        chapati = new JCheckBox("Chapati @ 20");
        tea = new JCheckBox("Tea @ 10");
        chips = new JCheckBox("Chips @ 100");
        stew = new JCheckBox("Stew @ 80");
        mandazi = new JCheckBox("Mandazi @ 15");

        riceBeans.setBounds(100, 100, 200, 20);
        chapati.setBounds(100, 150, 200, 20);
        tea.setBounds(100, 200, 200, 20);
        chips.setBounds(100, 250, 200, 20);
        stew.setBounds(100, 300, 200, 20);
        mandazi.setBounds(100, 350, 200, 20);

        riceBeans.setFont(new Font("Arial", Font.PLAIN, 20));
        chapati.setFont(new Font("Arial", Font.PLAIN, 20));
        tea.setFont(new Font("Arial", Font.PLAIN, 20));
        chips.setFont(new Font("Arial", Font.PLAIN, 20));
        stew.setFont(new Font("Arial", Font.PLAIN, 20));
        mandazi.setFont(new Font("Arial", Font.PLAIN, 20));

        b = new JButton("ORDER");
        b.setBounds(100, 400, 150, 50);
        b.setFont(new Font("Arial", Font.PLAIN, 30));
        b.setForeground(Color.white);
        b.setBackground(Color.darkGray);
        b.addActionListener(this);

        add(textHeader); add(riceBeans); add(chapati); add(tea); add(b); add(chips); add(stew); add(mandazi);
        add(Description);
        setSize(500, 600);
        setLayout(null);
        setVisible(true);
        setDefaultCloseOperation(EXIT_ON_CLOSE);
    }


    public static void main(String[] args) {
        new FoodOrderingSystem();
    }

    @Override
    public void actionPerformed(ActionEvent e) {

    }
}
