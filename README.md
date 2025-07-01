package ui;

import javax.swing.*;

public class UiExample {

    JFrame window = new JFrame("Example App");
    JPanel myPanel = new JPanel();
    JTextField emailField = new JTextField("Enter your email", 20); // Specify column width
    JButton myButton = new JButton("Click here");

    void drawUi() {
        myPanel.add(emailField);
        myPanel.add(myButton);
        window.add(myPanel);

        window.setSize(300, 500);
        window.setVisible(true);
        window.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }

    public static void main(String[] args) {
        // Ensure the GUI is created on the Event Dispatch Thread
        SwingUtilities.invokeLater(() -> {
            UiExample uiExample = new UiExample();
            uiExample.drawUi();
        });
    }
}
