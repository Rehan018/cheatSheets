## Table of Contents : 
- <b>[Importing Libraries](#importing-libraries)</b>
- <b>[Extend Class and Implement Interface >> Create Objects](#extend-class-and-implement-interfaces--create-objects)</b>
- <b>[Creating Constructor for default calling of GUI](#creating-constructor-for-default-calling-of-gui)</b>
- <b>[Creating JPanel](#creating-jpanel)</b>
- <b>[Adding Image icons in JPanel](#adding-image-icons-in-jpanel)</b>
- <b>[Add mouseListener to Exit icon](#add-mouselistener-to-exit-icon)</b>
- <b>[Add actionPerformed() method](#add-actionperformed()-method)</b>
- <b>[Socket Code in main class](#socket-code-in-main-class)</b>

<hr />

#### Importing Libraries

```

import javax.swing.*;     // for JFrame, JButton, Image ...
import java.awt.*;
import java.awt.event.*;  // for eventListener
import java.net.*;        // for socket
import java.io.*;         // for DataInputOutput
```

#### Extend Class and Implement Interface >> Create Objects

```
public class className extends JFrame implements ActionListener {
  JPanel p1;	
  JTextField t1;
  static ServerSocket skt;
  static Socket s;
  static DataInputStream din;
  static DataOutputStream dout;
```
  
#### Creating Constructor for default calling of GUI

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

#### Creating JPanel
<p>We can put multiple items in JPanel</p>

```
p1 = new JPanel();
p1.setLayout(null);
p1.setBackground(new Color(7, 84, 95));
p1.setBounds(0, 0, 400, 40);
add(p1);
```

#### Adding Image icons in JPanel

```
//Back Arrow .png
ImageIcon i1 = new ImageIcon(ClassLoader.getSystemResource("icons/back-arrow.png"));
Image i2 = i1.getImage().getScaledInstance(25, 25, Image.SCALE_DEFAULT);
ImageIcon i3 = new ImageIcon(i2);
JLabel l1 = new JLabel(i3);
l1.setBounds(8, 8, 25, 25);
p1.add(l1);	
```

#### Add mouseListener to Exit icon

```
l1.addMouseListener(new MouseAdapter() {
  public void mouseClicked(MouseEvent me) {
    System.exit(0);
  }
});
```

#### Add actionPerformed() method

```
public void actionPerformed(ActionEvent ae) {}
```

#### Socket Code in main class
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

