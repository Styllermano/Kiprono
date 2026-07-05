public RadioButtonDemo() {
    setTitle("RadioButtonDemo");
    setLayout(new FlowLayout());

    birdBtn = new JRadioButton("Bird");
    catBtn = new JRadioButton("Cat");
    dogBtn = new JRadioButton("Dog");
    rabbitBtn = new JRadioButton("Rabbit");
    pigBtn = new JRadioButton("Pig");

    ButtonGroup group = new ButtonGroup();
    group.add(birdBtn);
    group.add(catBtn);
    group.add(dogBtn);
    group.add(rabbitBtn);
    group.add(pigBtn);

    imageLabel = new JLabel();

    add(birdBtn); add(catBtn); add(dogBtn); add(rabbitBtn); add(pigBtn); add(imageLabel);

    birdBtn.addActionListener(this);
    catBtn.addActionListener(this);
    dogBtn.addActionListener(this);
    rabbitBtn.addActionListener(this);
    pigBtn.addActionListener(this);

    setSize(300, 300);
    setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    setVisible(true);
}

public void actionPerformed(ActionEvent e) {
    String pet = e.getActionCommand();
    JOptionPane.showMessageDialog(this, "You selected: " + pet);
    imageLabel.setIcon(new ImageIcon(pet.toLowerCase() + ".png"));
}

public static void main(String[] args) {
    new RadioButtonDemo();
}
