# 104021073
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.awt.event.WindowAdapter;
import java.awt.event.WindowEvent;
import java.awt.image.BufferedImage;
import java.io.File;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Random;

import javax.swing.Timer;

import javax.imageio.IIOException;
import javax.imageio.ImageIO;
import javax.swing.ImageIcon;
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JPanel;
public class x52 {
	
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Ha ha=new Ha();
		ha.setVisible(true);
	}
}
class Ha extends JFrame{
	 Timer timer;
	 int time=60;
	 int s=60;
	 int x=0;
	 Random ran = new Random();
	 int m=0;
;		static Button st=new Button("開始");
		static Button re=new Button("重新遊戲");
		static TextField sc=new TextField("分數");
		static TextField sc1=new TextField("0");
		static TextField ti=new TextField("時間");
	    static TextField ti1=new TextField("60");
	    static Button ti2=new Button("");
	 private Timer t1;
	
	 private Timer t2;
		
		public Ha(){
			hard();
				
			
		}

		private void hard() {
		



ImageIcon icon=new ImageIcon("d.png");

JButton b1=new JButton(icon);
JButton b2=new JButton(icon);
JButton b3=new JButton(icon);
JButton b4=new JButton(icon);
JButton b5=new JButton(icon);
JButton b6=new JButton(icon);
JButton b7=new JButton(icon);
JButton b8=new JButton(icon);
JButton b9=new JButton(icon);
b1.setBounds(100,100,80,80);
b2.setBounds(200,100,80,80);
b3.setBounds(300,100,80,80);
b4.setBounds(100,200,80,80);
b5.setBounds(100,300,80,80);
b6.setBounds(200,200,80,80);
b7.setBounds(300,200,80,80);
b8.setBounds(200,300,80,80);
b9.setBounds(300,300,80,80);
sc.setBounds(80, 30, 50, 20);
sc1.setBounds(130, 30, 50, 20);
ti.setBounds(350, 30, 50, 20);
ti1.setBounds(400, 30, 50, 20);
ti2.setBounds(400, 30, 50, 20);
this.setSize(500, 500);
this.setLocation(500, 250);
this.setVisible(true);
st.setBounds(100, 400, 100, 40);
re.setBounds(350, 400, 100, 40);
this.add(b1);
this.add(b2);
this.add(b3);
this.add(b4);
this.add(b5);
this.add(b6);
this.add(b7);
this.add(b8);
this.add(b9);
this.add(st);
this.add(re);
this.add(sc);
this.add(sc1);
this.add(ti);
this.add(ti1);
this.add(ti2);
sc.setEditable(false);
sc1.setEditable(false);
ti.setEditable(false);
ti1.setEditable(false);

this.addWindowListener(new WindowAdapter(){
	public void windowClosing(WindowEvent we){
		System.exit(0);
	}
});	

st.addActionListener(new ActionListener(){
	public void actionPerformed(ActionEvent ae){
		x=0;
		b1.hide();
		b2.hide();
		b3.hide();
		b4.hide();
		b5.hide();
		b6.hide();
		b7.hide();
		b8.hide();
		b9.hide();
		sc1.setText("0");
		st.hide();
		t1=new Timer((1000),new ActionListener(){	
			public void actionPerformed(ActionEvent ae){
				
				m=ran.nextInt(8);
				 
				if(m==0)
					b1.show();
				
				else if(m==1)
					b2.show();
				
				else if(m==2)
					b3.show();
				
				else if(m==3)
					b4.show();
				
				else if(m==4)
					b5.show();
				
				else if(m==5)
					b6.show();
				
				else if(m==6)
					b7.show();
				
				else if(m==7)
					b8.show();
				
				else if(m==8)
					b9.show();
				
			 
				ti1.setText(""+s);
				s--;
				if(s==-1){
					t1.stop();
					t2.stop();
					b1.hide();
					b2.hide();
					b3.hide();
					b4.hide();
					b5.hide();
					b6.hide();
					b7.hide();
					b8.hide();
					b9.hide();
				}
			}
		});
		t1.start();

		t2=new Timer((1500),new ActionListener(){	
			public void actionPerformed(ActionEvent ae){
				
					
				
				b1.hide();
				b2.hide();
				b3.hide();
				b4.hide();
				b5.hide();
				b6.hide();
				b7.hide();
				b8.hide();
				b9.hide();
			
			}
		});
		t2.start();
		
	}
});	

b1.addActionListener(new ActionListener(){
	public void actionPerformed(ActionEvent ae){
		x+=5;
		sc1.setText(""+x);
		b1.hide();
	}
});	
b2.addActionListener(new ActionListener(){
	public void actionPerformed(ActionEvent ae){
		x+=5;
		sc1.setText(""+x);
		b2.hide();
	}
});	
b3.addActionListener(new ActionListener(){
	public void actionPerformed(ActionEvent ae){
		x+=5;
		sc1.setText(""+x);
		b3.hide();
	}
});	
b4.addActionListener(new ActionListener(){
	public void actionPerformed(ActionEvent ae){
		x+=5;
		sc1.setText(""+x);
		b4.hide();
	}
});	
b5.addActionListener(new ActionListener(){
	public void actionPerformed(ActionEvent ae){
		x+=5;
		sc1.setText(""+x);
		b5.hide();
	}
});	
b6.addActionListener(new ActionListener(){
	public void actionPerformed(ActionEvent ae){
		x+=5;
		sc1.setText(""+x);
		b6.hide();
	}
});	
b7.addActionListener(new ActionListener(){
	public void actionPerformed(ActionEvent ae){
		x+=5;
		sc1.setText(""+x);
		b7.hide();
	}
});	
b8.addActionListener(new ActionListener(){
	public void actionPerformed(ActionEvent ae){
		x+=5;
		sc1.setText(""+x);
		b8.hide();
	}
});	
b9.addActionListener(new ActionListener(){
	public void actionPerformed(ActionEvent ae){
		x+=5;
		sc1.setText(""+x);
		b9.hide();
	}
});	
re.addActionListener(new ActionListener(){
	public void actionPerformed(ActionEvent ae){
		t1.stop();
		t2.stop();
		s=60;
		x=0;
		ti1.setText("60");
		sc1.setText("0");
				st.show();
				b1.hide();
				b2.hide();
				b3.hide();
				b4.hide();
				b5.hide();
				b6.hide();
				b7.hide();
				b8.hide();
				b9.hide();
	}
});	
	}

}
