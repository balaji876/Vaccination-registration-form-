# Vaccination-registration-form-
package awt;

import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

class MyFrame
	extends JFrame
	implements ActionListener {

	private Container c;
	private JLabel title;
	private JLabel name;
	private JTextField tname;
	private JLabel mno;
	private JTextField tmno;
	private JLabel gender;
	private JRadioButton male;
	private JRadioButton female;
	private ButtonGroup gengp;
	private JLabel dob;
	private JComboBox date;
	private JComboBox month;
	private JComboBox year;
	private JLabel vdat;
	private JComboBox date1;
	private JComboBox month1;
	private JComboBox year1;
	private JComboBox vdose;
	private JTextField tname1;
	private JLabel add;
	private JTextArea tadd;
	private JCheckBox term;
	private JButton sub;
	private JButton reset;
	private JTextArea tout;
	private JLabel res;
	private JTextArea resadd;

	private String dates[]
		= { "1", "2", "3", "4", "5",
			"6", "7", "8", "9", "10",
			"11", "12", "13", "14", "15",
			"16", "17", "18", "19", "20",
			"21", "22", "23", "24", "25",
			"26", "27", "28", "29", "30",
			"31" };
	private String months[]
		= { "Jan", "feb", "Mar", "Apr",
			"May", "Jun", "July", "Aug",
			"Sup", "Oct", "Nov", "Dec" };
	private String years[]
		= { "Before","1969", "1970", "1971",
			"1972", "1973", "1974", "1975",
			"1976", "1977", "1978", "1979",
			"1980", "1981", "1982", "1983",
			"1984", "1985", "1986", "1988",
			"1987", "1988", "1989", "1990",
			"1991", "1992", "1993", "1994",
			"1995", "1996", "1997", "1998",
			"1999", "2000", "2001", "2002",
			"2003", "2004", "2005", "2006",
			"2007", "2008", "2009", "2010",
			"2011", "2012", "2013", "2014",
			"2015", "2016", "2017", "2018",
			"2019", "2020", "2021", "2022"};
	
	private String dates1[]
			= { "1", "2", "3", "4", "5",
				"6", "7", "8", "9", "10",
				"11", "12", "13", "14", "15",
				"16", "17", "18", "19", "20",
				"21", "22", "23", "24", "25",
				"26", "27", "28", "29", "30",
				"31" };
		private String months1[]
			= { "Jan", "feb", "Mar", "Apr",
				"May", "Jun", "July", "Aug",
				"Sup", "Oct", "Nov", "Dec" };
		private String years1[]
			= { "2020", "2021 ","2022", "2023"};

	public MyFrame()
	{
		setTitle("Covid Vaccine Form");
		setBounds(300, 90, 900, 600);
		setDefaultCloseOperation(EXIT_ON_CLOSE);
		setResizable(true);

		c = getContentPane();
		c.setLayout(null);

		title = new JLabel("Covid Vaccine Registration Form");
		title.setFont(new Font("Arial", Font.BOLD, 30));
		title.setSize(800, 30);
		title.setLocation(200, 30);
		c.add(title);

		name = new JLabel("Name:");
		name.setFont(new Font("Arial", Font.PLAIN, 20));
		name.setSize(100, 20);
		name.setLocation(100, 100);
		c.add(name);

		tname = new JTextField();
		tname.setFont(new Font("Arial", Font.PLAIN, 15));
		tname.setSize(190, 20);
		tname.setLocation(200, 100);
		c.add(tname);

		mno = new JLabel("Mobile No:");
		mno.setFont(new Font("Arial", Font.PLAIN, 20));
		mno.setSize(100, 20);
		mno.setLocation(100, 135);
		c.add(mno);

		tmno = new JTextField();
		tmno.setFont(new Font("Arial", Font.PLAIN, 15));
		tmno.setSize(150, 20);
		tmno.setLocation(200, 135);
		c.add(tmno);

		gender = new JLabel("Gender:");
		gender.setFont(new Font("Arial", Font.PLAIN, 20));
		gender.setSize(100, 20);
		gender.setLocation(100, 175);
		c.add(gender);

		male = new JRadioButton("Male");
		male.setFont(new Font("Arial", Font.PLAIN, 15));
		male.setSelected(true);
		male.setSize(75, 20);
		male.setLocation(200, 175);
		c.add(male);

		female = new JRadioButton("Female");
		female.setFont(new Font("Arial", Font.PLAIN, 15));
		female.setSelected(false);
		female.setSize(80, 20);
		female.setLocation(275, 175);
		c.add(female);

		gengp = new ButtonGroup();
		gengp.add(male);
		gengp.add(female);

		dob = new JLabel("D.O.B:");
		dob.setFont(new Font("Arial", Font.PLAIN, 20));
		dob.setSize(100, 20);
		dob.setLocation(100, 210);
		c.add(dob);

		date = new JComboBox(dates);
		date.setFont(new Font("Arial", Font.PLAIN, 15));
		date.setSize(50, 20);
		date.setLocation(200, 210);
		c.add(date);

		month = new JComboBox(months);
		month.setFont(new Font("Arial", Font.PLAIN, 15));
		month.setSize(60, 20);
		month.setLocation(250, 210);
		c.add(month);

		year = new JComboBox(years);
		year.setFont(new Font("Arial", Font.PLAIN, 15));
		year.setSize(60, 20);
		year.setLocation(320, 210);
		c.add(year);
		
		vdat = new JLabel("vacination date:");
		vdat.setFont(new Font("Arial", Font.PLAIN, 20));
		vdat.setSize(200, 20);
		vdat.setLocation(50, 253);
		c.add(vdat);

		date1 = new JComboBox(dates1);
		date1.setFont(new Font("Arial", Font.PLAIN, 15));
		date1.setSize(50, 20);
		date1.setLocation(200, 253);
		c.add(date1);

		month1 = new JComboBox(months1);
		month1.setFont(new Font("Arial", Font.PLAIN, 15));
		month1.setSize(60, 20);
		month1.setLocation(250, 253);
		c.add(month1);

		year1 = new JComboBox(years1);
		year1.setFont(new Font("Arial", Font.PLAIN, 15));
		year1.setSize(60, 20);
		year1.setLocation(320, 253);
		c.add(year1);
		
		name = new JLabel("Vaccine Name&Dose:");
		name.setFont(new Font("Arial", Font.PLAIN, 20));
		name.setSize(250, 20);
		name.setLocation(10, 288);
		c.add(name);

		tname1 = new JTextField();
		tname1.setFont(new Font("Arial", Font.PLAIN, 15));
		tname1.setSize(180, 20);
		tname1.setLocation(210, 288);
		c.add(tname1);

		add = new JLabel("Address:");
		add.setFont(new Font("Arial", Font.PLAIN, 20));
		add.setSize(100, 20);
		add.setLocation(100, 340);
		c.add(add);
		

		tadd = new JTextArea();
		tadd.setFont(new Font("Arial", Font.PLAIN, 15));
		tadd.setSize(200, 75);
		tadd.setLocation(200, 320);
		tadd.setLineWrap(true);
		c.add(tadd);

		term = new JCheckBox("Accept Terms And Conditions.");
		term.setFont(new Font("Arial", Font.PLAIN, 15));
		term.setSize(250, 20);
		term.setLocation(150, 410);
		c.add(term);

		sub = new JButton("Submit");
		sub.setFont(new Font("Arial", Font.PLAIN, 15));
		sub.setSize(100, 20);
		sub.setLocation(150, 450);
		sub.addActionListener(this);
		c.add(sub);

		reset = new JButton("Reset");
		reset.setFont(new Font("Arial", Font.PLAIN, 15));
		reset.setSize(100, 20);
		reset.setLocation(270, 450);
		reset.addActionListener(this);
		c.add(reset);

		tout = new JTextArea();
		tout.setFont(new Font("Arial", Font.PLAIN, 15));
		tout.setSize(300, 400);
		tout.setLocation(500, 100);
		tout.setLineWrap(true);
		tout.setEditable(false);
		c.add(tout);

		res = new JLabel("");
		res.setFont(new Font("Arial", Font.PLAIN, 20));
		res.setSize(500, 25);
		res.setLocation(100, 500);
		c.add(res);

		resadd = new JTextArea();
		resadd.setFont(new Font("Arial", Font.PLAIN, 15));
		resadd.setSize(200, 75);
		resadd.setLocation(580, 175);
		resadd.setLineWrap(true);
		c.add(resadd);

		setVisible(true);
	}

	public void actionPerformed(ActionEvent e)
	{
		System.out.println("");
		if (e.getSource() == sub) {
			if (term.isSelected()) {
				
				String data1;
				String data
					= "Your Details Are:\n--------------------------\n"
				    +"Name : "
					+ tname.getText() + "\n"
					+ "Mobile : "
					+ tmno.getText() + "\n"
				    +"vdose:"
				    +tname1.getText() +"\n";
				if (male.isSelected())
					data1 = "Gender : Male"
							+ "\n";
				else
					data1 = "Gender : Female"
							+ "\n";
				
				String data2
					= "DOB : "
					+ (String)date.getSelectedItem()
					+ "/" + (String)month.getSelectedItem()
					+ "/" + (String)year.getSelectedItem()
					+ "\n";
				
				String data3
				   = "vdate : "
				   + (String)date1.getSelectedItem()
			   	   + "/" + (String)month1.getSelectedItem()
				   + "/" + (String)year1.getSelectedItem()
				   + "\n";
				
				String data4 = "Address : " + tadd.getText()+"\n-------------------------\n##^^GetVax to celebrate a healthier future^^##\n\n--------------\nFor More details:contact LIVEWIRESELAIYUR\nPhoneNo:9384664005";
				tout.setText(data + data1 + data2 + data3 + data4);
				tout.setEditable(false);
				res.setText("Registered Successfully...");
			}
			else {
				tout.setText("");
				resadd.setText("");
				res.setText("Please accept the"
							+ " terms & conditions..");
			}
		}

		else if (e.getSource() == reset) {
			String def = "";
			tname.setText(def);
			tadd.setText(def);
			tmno.setText(def);
			res.setText(def);
			tout.setText(def);
			term.setSelected(false);
			date.setSelectedIndex(0);
			month.setSelectedIndex(0);
			year.setSelectedIndex(0);
			date1.setSelectedIndex(0);
			month1.setSelectedIndex(0);
			year1.setSelectedIndex(0);
			tname1.setText(def);
			resadd.setText(def);
		}
	}
}

class Registration {

	public static void main(String[] args) throws Exception
	{
		MyFrame f = new MyFrame();
	}
}
