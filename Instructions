package projectBackup;

import java.awt.GridLayout;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.io.BufferedReader;
import java.io.File;
import java.io.FileReader;
import java.io.IOException;
import javax.swing.ButtonGroup;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JPanel;
import javax.swing.JRadioButton;
public class Instructions extends JFrame implements ActionListener {
	private static final long serialVersionUID = 1L;
	@Override
	public void actionPerformed(ActionEvent arg0) {
		setTitle("Ingredients");
		setDefaultCloseOperation(EXIT_ON_CLOSE);
		setSize(550, 500);
		setLayout(new GridLayout());
		setVisible(true);
		setLocationRelativeTo(null);
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		File file = new File(
				"C:/Users/soumik/Workspace/jar files here/Project/Beta V0.0.3/instruction.txt");
		BufferedReader reader = null;
		JPanel panel = new JPanel();
		try {
			reader = new BufferedReader(new FileReader(file));
			String text = null;
			//int i = 0;
			while ((text = reader.readLine()) != null) {
				JRadioButton r = new JRadioButton();
				ButtonGroup bg = new ButtonGroup();
				JLabel label1 = new JLabel(text);
				bg.add(r);
				panel.add(label1);
				panel.add(r);
			}
			reader.close();
			getContentPane().add(panel);
		} catch (IOException e) {
			e.printStackTrace();
		}
	}
}
