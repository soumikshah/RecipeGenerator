package projectBackup;

import java.awt.GridLayout;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.io.File;
import java.io.IOException;
import java.util.Scanner;
import javax.swing.JButton;
import javax.swing.JCheckBox;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JPanel;
import javax.swing.JTextField;
public class ControlPanel1 extends JFrame {
	private static final long serialVersionUID = 1L;
	JTextField textfield;
	String ingredient;
	double quantity;
	String unit;

	public ControlPanel1() {
		setTitle("Hw5");
		setLayout(new GridLayout());
		setSize(250, 300);
		// Scanner sc = new Scanner(System.in);
		setDefaultCloseOperation(EXIT_ON_CLOSE);
		JPanel p1 = new JPanel();
		JButton button1 = new JButton("Update");
		JLabel Label = new JLabel();
		textfield = new JTextField("Type number of ppl here");
		p1.add(Label);
		p1.add(textfield);
		p1.add(button1);
		button1.addActionListener(new Ingredients());
		getContentPane().add(p1);
		setVisible(true);
		setLocationRelativeTo(null);
	}

	public static void main(String args[]) {
		new ControlPanel1();
	}

	public class Ingredients extends JFrame implements ActionListener {
		private static final long serialVersionUID = 1L;

		@Override
		public void actionPerformed(ActionEvent arg0) {
			setTitle("Ingredients");
			setDefaultCloseOperation(EXIT_ON_CLOSE);
			setSize(140, 430);
			setLayout(new GridLayout());
			setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
			setLocationRelativeTo(null);
			int Message = Integer.parseInt(textfield.getText());
			JPanel panel = new JPanel();
			File file = new File(
					"C:/Users/soumik/Workspace/jar files here/Project/Beta V0.0.3/ingredient.txt");
			// StringBuilder line = new StringBuilder();
			//BufferedReader reader = null;
			Scanner reader;
			try {
				reader=new Scanner(file);
				while (reader.hasNextLine()) {
					String str = reader.nextLine();
					String [] a = str.split(" ");
					String ingredient=a[0];
					double quantity=Double.parseDouble(a[1]);
					String unit=a[2];
					JCheckBox cb = new JCheckBox();
					JLabel label1 = new JLabel(ingredient+" "+quantity*Message+" "+unit);
					panel.add(cb);
					panel.add(label1);
				}
				reader.close();
				JButton ingredients = new JButton("Go to Instructions now");
				ingredients.addActionListener(new Instructions());
				panel.add(ingredients);
				getContentPane().add(panel);
			} catch (IOException e) {
				e.printStackTrace();
			}
			setVisible(true);
		}
	}
}

