package projeto_copa;
import javax.swing.*;

public class tela_log {

	public static void main(String[] args) {
		
		JFrame j=new JFrame("Tela de Login");
		j.setSize(300,200);
		j.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		j.setLayout(null);
		j.setLocationRelativeTo(null);
		
		JLabel labU=new JLabel("Usuarios:");
		labU.setBounds(20,20,80,25);
		j.add(labU);
		
		JTextField camU=new JTextField();
		camU.setBounds(100,20,160,25);
		j.add(camU);
		
		JLabel labS=new JLabel("Senha:");
		labS.setBounds(20,50,80,25);
		j.add(labS);
		
		JPasswordField camS=new JPasswordField();
		camS.setBounds(100,50,160,25);
		j.add(camS);
		
		JButton botL=new JButton("Entrar");
		botL.setBounds(100,90,100,25);
		j.add(botL);
		
		botL.addActionListener(e -> {
			
			String usu = camU.getText();
			String sen = new String(camS.getPassword());
			
			if (usu.equals("boot") && sen.equals("69")) {
				JOptionPane.showMessageDialog(j,"Login Realizado");
				j.dispose();
				new menuInicial();
			}else {
				JOptionPane.showMessageDialog(j,"Login Incorreto nob","Erro",JOptionPane.ERROR_MESSAGE);
				camU.setText("");
				camS.setText("");
			}
			
		});
		
		j.setVisible(true);
	
	}

}
