# tutorial

package chyderabot;

import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

import javax.swing.*;

public class chyderaBot extends JFrame {
   static JTextArea txt=new JTextArea();
   static JTextField field=new JTextField();
	public static void main(String[] args) {
		JFrame frame= new JFrame();
		frame.setVisible(true);
		frame.setDefaultCloseOperation(EXIT_ON_CLOSE);
		frame.setSize(500,500);
		frame.setLayout(null);
		frame.setTitle("chyderabot");
		frame.add(field);
		frame.add(txt);
		txt.setLocation(1,1);
		txt.setSize(500,400);
		field.setLocation(1,400);;
		field.setSize(500,40);
		field.addActionListener(new ActionListener() {

			@Override
			public void actionPerformed(ActionEvent arg0) {
				String msg=field.getText();
				txt.append("You= "+msg+"\n");
				field.setText("");
				if(msg.toLowerCase().contains("hi"))
				{
					txt.append("Bot >> Hi! How you doing?\n");
				}
				else if(msg.toLowerCase().contains("how are you doing?")) 
				{
					txt.append("Bot >> I am doing fine and you?\n");
			}
			else if(msg.toLowerCase().contains("am doing fine")) 
			{
				txt.append("Bot >> okay, so how can i help you?\n");
			}
			else if(msg.toLowerCase().contains("i am sad")) 
			{
				txt.append("Bot >> Awwn,sorry dear.So how can i help you?\n");
			}
			else if(msg.toLowerCase().contains("what is coronavirus?")) 
			{
				txt.append("Bot =>> Coronavirus also  known as covid-19 is a disease caused by a \n new strain of coronavirus (SARS-CoV-2) that has not been previously \n identified in humans.\n");
			}
			else if(msg.toLowerCase().contains("where did coronavirus breakout from?")) 
			{
				txt.append("Bot >> The virus broke out from a pace in China called WUHAN.\n");
			}	
			else if(msg.toLowerCase().contains("when did it breakout?")) 
			{
				txt.append("Bot >> It was reported to World Health Organization(WHO) on the \n '31st of December 2019'.\n");
			}	
			else if(msg.toLowerCase().contains("how many country has the virus?")) 
			{
				txt.append("Bot >>There are about 188 countries affected eith the virus.\n");
			}	
			else if(msg.toLowerCase().contains("what are the number of infected people in the world?")) 
			{
				txt.append("Bot >> As of Today,there are about over 9millions cases and \n 0ver 46 thousand death.\n");
			}	
			else if(msg.toLowerCase().contains("how many people have the virus in nigeria?")) 
			{
				txt.append("Bot >> The number of infected people in nigeria as of today are  19,808.\n");
			}
			else if(msg.toLowerCase().contains("how can someone be prevented from contracting the virus?")) 
			{
				txt.append("Bot >> You are expeected to WASH YOUR HANDS always or use an \n ALCOHOL-BASE SANITIZER, use a FACE MASK and maintaining \n SOCIAL DISTANCING.");
			}
			else 
			{
				
				txt.append("Bot >> I don't understand,\n check if you omitted a QUESTION MARK,a letter in your spellings \n or maybe you aren't using either 'what', 'where', or 'how'\n");
			}
				
}
			});
	}

}
