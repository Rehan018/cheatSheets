# Swing
<p><b>Importing Libraries : </b></p>

```

import javax.swing.*;     // for JFrame, JButton, Image ...
import java.awt.*;
import java.awt.event.*;  // for eventListener
import java.net.*;        // for socket
import java.io.*;         // for DataInputOutput
```

<p><b>Extend Class and Implement Interface >> Create Objects</b></p>

```
public class className extends JFrame implements ActionListener {
  JPanel p1;	
  JTextField t1;
  static ServerSocket skt;
  static Socket s;
  static DataInputStream din;
  static DataOutputStream dout;
```
  
<p><b>Creating Constructor for default calling of GUI</b></p>

```
className(){
  // codes
  
  setLayout(null);
  setLocation(200, 100);
  setSize(400, 600);
  setUndecorated(true);
  setVisible(true);
}
    
```

<p><b>Creating JPanel</b></p>
<p>We can put multiple items in JPanel</p>

```
p1 = new JPanel();
p1.setLayout(null);
p1.setBackground(new Color(7, 84, 95));
p1.setBounds(0, 0, 400, 40);
add(p1);
```

<p><b>Adding Image icons in JPanel</b></p>

```
//Back Arrow .png
ImageIcon i1 = new ImageIcon(ClassLoader.getSystemResource("icons/back-arrow.png"));
Image i2 = i1.getImage().getScaledInstance(25, 25, Image.SCALE_DEFAULT);
ImageIcon i3 = new ImageIcon(i2);
JLabel l1 = new JLabel(i3);
l1.setBounds(8, 8, 25, 25);
p1.add(l1);	
```

<p><b>Add mouseListener to Exit icon</b></p>

```
l1.addMouseListener(new MouseAdapter() {
  public void mouseClicked(MouseEvent me) {
    System.exit(0);
  }
});
```

<p><b>Add actionPerformed() method</b></p>

```
public void actionPerformed(ActionEvent ae) {}
```

<p><b>Socket Code in main class</b></p>
<b>Server</b>

```
try{
  skt = new ServerSocket(6008);
  s = skt.accept();

  din = new DataInputStream(s.getInputStream());
  dout = new DataOutputStream(s.getOutputStream());

  while(true) {
    msgin = din.readUTF();
    a1.setText(a1.getText() + "\n" + msgin);
  }

  //skt.close();
  //s.close();

}
catch(Exception e) {
  //blank
}
```

<b>Client</b>

```
try {
  s = new Socket("127.0.0.1", 6008);

  din = new DataInputStream(s.getInputStream());
  dout = new DataOutputStream(s.getOutputStream());

  while(true) {
    msgin = din.readUTF();
    a1.setText(a1.getText() + "\n" + msgin);
  }

  //s.close();

}
catch(Exception e) {
  //blank
}
```

