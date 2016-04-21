# ananchen
package game;

import java.util.Scanner;

public class Lucky {
	static String name;
	static int password;
	static int number;
	static boolean flog=true;
	static int a=0;
	public static int mune()
	{
		System.out.println("***************��ӭʹ�����˳齱ϵͳ************");
		System.out.println("1.ע��\t2.��½\t3.�齱��\t4.�˳� ");
		Scanner input=new Scanner(System.in);
		int num=input.nextInt();
		return num;
		
	}
	
	public static void regist()
	{
		System.out.println("�������û���");
		Scanner input=new Scanner(System.in);
		name=input.nextLine();
		System.out.println("��������");
		password=input.nextInt();
		number=(int)(Math.random()*10);
		System.out.println("ע��ɹ������ס�����û���������");
		System.out.println("�û���"+name);
		System.out.println("��Ա��"+number);
	
		
		
	}//ע��
	public static void login()
	{
		int use_password;
		String use_name;
		System.out.println("������Ҫ��½���û���");
		Scanner input=new  Scanner(System.in);
		do{
		use_name=input.nextLine();
		if(name.equals(use_name))
		{
			System.out.println("���������룺");
			use_password=input.nextInt();
			for(int i=0;i<3;i++){
				if(i>=3){
					System.out.println("�������3�Σ��˳�����");return;}
			if(password==use_password)
			{
				System.out.println("������ȷ����½�ɹ�");
				a=1;
				return;
			}else
			{
				System.out.println("��������˳�����");
				return;
			}
			
			}
			
		}else
		{
			System.out.println("�û�����������������");
		}
		}while(!(name.equals(use_name)));
	}//��¼
	public static void luck()
	{
		int lucknum[]=new int[5];  
		int use_number;
		//String use_name;
		
		for (int i = 0; i <lucknum.length; i++) {
			lucknum[i]=(int)(Math.random()*10);
		}
		if(a==1){
		System.out.println("��ӭ����齱���ڣ�");
		System.out.println("�������Ա�ţ�");
		Scanner input =new Scanner(System.in);
		use_number=input.nextInt();
		int j;
		for ( j = 0; j < lucknum.length; j++) {
			if(use_number==lucknum[j])
			{
				System.out.println("��ϲ���н��ˣ�");
				break;
				
			}
			}
			if(j>=lucknum.length)
			System.out.println("���ź�û���н�~���н������ǣ�");
			
			
		
			
			for (int i = 0; i < lucknum.length; i++) {
				System.out.println(lucknum[i]);
			}
			
		//flog=false;
		System.out.println("�������ô��Y?N?");
		//System.out.println("GGGGG");
		String a;
		a=input.next();
		if(a.equals("Y")){
			flog=true;
		     return;}
		if(a.equals("N"))
		{
			flog=false;
					return;
		}
		
	
		//Scanner input=new Scanner(System.in);
		
		}
		else
		{
			System.out.println("���ȵ�¼~");
			
		}
		return ;
				}

		
		
	
		
		
		
	
	
	public static void main(String[] args) {
       int n;
   
       
       while(flog){
       n=mune();
		switch (n) {
		case 1:regist();
			break;
		case 2:login();
			//��½
			break;
		case 3:luck();
			//�齱
			break;
		case 4:return;
			//�˳�			break;

		default:
			System.out.println("�������");
			break;
		}
	
	}

	}
}

