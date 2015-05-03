import javax.swing.*;
import javax.swing.event.*;
import java.awt.*;
import java.awt.event.*;
public class TestRefreshCard extends JFrame implements ActionListener{
	private ImageIcon[] card = new ImageIcon[4];//New an ImageIcon array and define it 
	private JButton jbt = new JButton("Refresh");//new a JButton 
	private JLabel[] c = new JLabel[4];//new a JLabel array and define
	JPanel p1 = new JPanel();//New a JPanel
	//method
	public void pokercard(){
		int[] deck = new int[54];//Create a deck array to store 54 cards
		for(int i = 0;i<deck.length ;i++) // Initialize cards 
			deck[i] = i;
		for(int i = 0;i<deck.length;i++){// Shuffle the cards
			int index =(int)(Math.random()*54);
			int temp = deck[i];
			deck[i] = deck[index];
			deck[index] = temp;
		}
		for(int i = 0;i<4;i++){
			card[i] = new ImageIcon(getClass().getResource("card/"+(deck[i]+1)+".png"));//put the first 4 cards in card array and find the images 
		}
	}
		
	//Constructor
	public TestRefreshCard(){
		int [] deck = new int[54];//Create a deck array to store 54 cards
		for(int i = 0;i<deck.length ;i++)// Initialize cards 
			deck[i] = i;
		for(int i = 0;i<deck.length;i++){// Shuffle the cards
			int index = (int)(Math.random()*54);
			int temp = deck[i];
			deck[i] = deck[index];
			deck[index] = temp;
		}
		for(int i = 0;i<4;i++){
			card[i] = new ImageIcon(getClass().getResource("card/"+(deck[i]+1)+".png"));//put the first 4 cards in card array and find the images 
		}
		setLayout(new FlowLayout());//Set a Flowlayout 
		for(int i = 0;i<4;i++){
			c[i] = new JLabel(card[i]);//cards in JLable
			add(c[i]);//add it on the screen
		}
		p1.setBorder(BorderFactory.createLineBorder(Color.LIGHT_GRAY));//set border in gray color
		add(p1,BorderLayout.SOUTH);//add the p1 panel in the south of frame
		p1.add(jbt);//add the p1 of button 
		jbt.addActionListener(this);//add addictionlistener
	}
	
	
	 public void actionPerformed(ActionEvent e) {//code that reacts to the action
		 if(e.getSource()==jbt){
			pokercard();
			for(int i = 0;i<4;i++){
				c[i].setIcon(card[i]);
			}
		 }
	 }
	public static  void main(String[] args){
		TestRefreshCard frame = new TestRefreshCard();//create a frame
		frame.setTitle("TestRefreshCard");//frame name 
		frame.setSize(400,200);//frame size
		frame.setLocationRelativeTo(null);//center a frame
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);//close upon exit
		frame.setVisible(true);//display the frame
		frame.setResizable(false);//can not set the frame size
	}
}
