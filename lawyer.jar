import java.awt.Color;
import java.awt.Container;
import java.awt.Font;
import java.awt.GridLayout;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JPanel;
import javax.swing.JTextArea;

public class Game {
	
	JFrame window;
	Container con;
	JPanel titleNamePanel, startButtonPanel, mainTextPanel, choiceButtonPanel;
	JLabel titleNameLabel;
	Font titleFont = new Font("Courier New", Font.PLAIN, 100);
	Font normalFont = new Font("Courier New",Font.PLAIN, 28);
	JButton startButton, choice1, choice2, choice3;
	JTextArea mainTextArea;
	String position;
	
	TitleScreenHandler tsHandler = new TitleScreenHandler();
	ChoiceHandler choiceHandler = new ChoiceHandler();
	

	public static void main(String[] args) {

		new Game();
	}
	
	public Game(){
		
		window = new JFrame();
		window.setSize(800, 600);
		window.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		window.getContentPane().setBackground(Color.black);
		window.setLayout(null);
		window.setVisible(true);
		con = window.getContentPane();
		
		titleNamePanel = new JPanel();
		titleNamePanel.setBounds(100, 100, 600, 150);
		titleNamePanel.setBackground(Color.black);
		titleNameLabel = new JLabel("Lawyer");
		titleNameLabel.setForeground(Color.white);
		titleNameLabel.setFont(titleFont);
		
		
		startButtonPanel = new JPanel();
		startButtonPanel.setBounds(300, 400, 200, 100);
		startButtonPanel.setBackground(Color.black);
		
		startButton = new JButton("START");
		startButton.setBackground(Color.black);
		startButton.setForeground(Color.white);
		startButton.setFont(normalFont);
		startButton.addActionListener(tsHandler);
		startButton.setFocusPainted(false);
		
		titleNamePanel.add(titleNameLabel);
		startButtonPanel.add(startButton);
		
		con.add(titleNamePanel);
		con.add(startButtonPanel);
	}
	
    public void createGameScreen(){
    	
    	titleNamePanel.setVisible(false);
    	startButtonPanel.setVisible(false);
    	
    	mainTextPanel = new JPanel();
    	mainTextPanel.setBounds(100, 100, 600, 250);
    	mainTextPanel.setBackground(Color.black);
    	con.add(mainTextPanel);
    	
    	mainTextArea = new JTextArea("Your Are Kevin Lomax a simple Lawyer,you come from Florida,you are a young and brilliant lawyer and you have never lost a single trial in you life.You had to choose your destiny between E and G");
    	position = "lawyer";
    	mainTextArea.setBounds(100, 100, 600, 250);
    	mainTextArea.setBackground(Color.black);
    	mainTextArea.setForeground(Color.white);
    	mainTextArea.setFont(normalFont);
    	mainTextArea.setLineWrap(true);
    	mainTextPanel.add(mainTextArea); 
    	
    	choiceButtonPanel = new JPanel();
    	choiceButtonPanel.setBounds(258, 350, 300, 150);
    	choiceButtonPanel.setBackground(Color.black);
    	choiceButtonPanel.setLayout(new GridLayout(4,1));
    	con.add(choiceButtonPanel);
    	
    	choice1 = new JButton("E");
    	choice1.setBackground(Color.black);
    	choice1.setForeground(Color.white);
    	choice1.setFont(normalFont);  
    	choice1.setFocusPainted(false);
    	choice1.addActionListener(choiceHandler);
    	choice1.setActionCommand("c1");
    	choiceButtonPanel.add(choice1);
    	choice2 = new JButton("G");
    	choice2.setBackground(Color.black);
    	choice2.setForeground(Color.white);
    	choice2.setFont(normalFont);
    	choice2.setFocusPainted(false);
    	choice2.addActionListener(choiceHandler);
    	choice2.setActionCommand("c2");
    	choiceButtonPanel.add(choice2);
    	choice3 = new JButton("Back");
    	choice3.setBackground(Color.black);
    	choice3.setForeground(Color.white);
    	choice3.setFont(normalFont);
    	choice3.setFocusPainted(false);
    	choice3.addActionListener(choiceHandler);
    	choice3.setActionCommand("c3");
    	choiceButtonPanel.add(choice3);
    	
    }
    public void E(){
    	position = "E";
    	mainTextArea.setText("It’s 7:00 in Florida, you and your wife are back where you belong. \nIn a hearing opposing a professor \nnamed Getty who is accused of \ns***********.");
    	choice1.setText("Y");
    	choice2.setText("N");
    	choice3.setText("Back");
    }
  
    public class TitleScreenHandler implements ActionListener{
    	
    	public void actionPerformed(ActionEvent event){
    		
    		createGameScreen();
    	}
     }
    public class ChoiceHandler implements ActionListener{
    	
    	public void actionPerformed(ActionEvent event){
    		
    		String yourChoice = event.getActionCommand();
    		
    		switch(position){
    		case "lawyer":
    			switch(yourChoice){
    			case "c1": E(); break;
    			case "c2": break;
    			case "c3": break;
    			}
    			break;
    		case "E": 
    			switch(yourChoice){
    			case "c3": lawyer(); break;
    			}
    			
    		}
    		
    		
    	}

		public void lawyer() {
			position = "lawyer";
			mainTextArea.setText("Your Are Kevin Lomax a simple Lawyer,you come from Florida,you are a young and brilliant lawyer and you have never lost a single trial in you life.You had to choose your destiny between E and G");
	    	choice1.setText("E");
	    	choice2.setText("G");
	    	choice3.setText("Back");
		}
    }
}
