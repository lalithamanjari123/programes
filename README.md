import java.util.Scanner;
import java.util.Random;
class RandomGame
{
    public static void main(String args[])
    {
        Scanner sc=new Scanner(System.in);
        Random r=new Random();
        int flag=0;
        int i=0;
        int choice=0,system_num,user_num;
        while(choice!=3)
        {
            System.out.println("Press\n for round1-1\n for round2-2\n 3 for exit");
            choice=sc.nextInt();
            switch(choice)
            {
            case 1:
                System.out.println("Round1 consistes of 10 chances\n");
                system_num=r.nextInt(100);
                while(flag==0&&i!=10)
                {
                    System.out.println("Enter your number");
                    user_num=sc.nextInt();
                    if(system_num>user_num)
                    {
                        i=i+1;
                        System.out.println("you have entered less number than system number\nyou have another"+(10-i));
                    }
                    else if(system_num<user_num)
                    {
                        i=i+1;
                        System.out.println("you have entered great number than system number\nyou have another"+(10-i));
                    }
                    else if(system_num==user_num)
                    {
                        flag=1;
                        System.out.println("Congratulations!!! your score is"+(100-10*i));
                    }
                    else if(i==10)
                    {
                        System.out.println("sorry!! better luck next time\n your score is 0");
                    }
                }
                break;
             case 2:
                flag=0;
                System.out.println("Round2 consistes of 5 chances\n");
                system_num=r.nextInt(100);
                while(flag==0&&i!=5)
                {
                    System.out.println("Enter your number");
                    user_num=sc.nextInt();
                    if(system_num>user_num)
                    {
                        i=i+1;
                        System.out.println("you have entered less number than system number\nyou have another"+(5-i));
                    }
                    else if(system_num<user_num)
                    {
                        i=i+1;
                        System.out.println("you have entered great number than system number\nyou have another"+(5-i));
                    }
                    else if(system_num==user_num)
                    {
                        flag=1;
                        System.out.println("Congratulations!!! your score is"+(100-20*i));
                    }
                    else if(i==5)
                    {
                        System.out.println("sorry!! better luck next time\n your score is 0");
                    }
                }
                break;
            }
        }
    };
};
