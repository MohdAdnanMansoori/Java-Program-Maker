package upkssv;
import java.util.*;
public class patt
{
    public static void main()
    {
        patt obj=new patt();
        int i,j,rows,n,t,freq,d,a,num;
        Scanner sc=new Scanner(System.in);
        System.out.print("Enter no. of rows: ");
        rows=sc.nextInt();
        int p[]=new int[rows];
        int f[]=new int[rows];
        int l[]=new int[rows];
        System.out.println("Enter pattern");
        for(i=0;i<rows;i++)
          p[i]=sc.nextInt();
        for(i=0;i<rows;i++)
        {
            t=0;
            n=p[i];
            l[i]=n%10;
            while(n!=0)
            {   t++;
                n/=10;   }
            if(t>1)
            f[i]=p[i]/(int)(Math.pow(10,t-1));
            else
            f[i]=p[i];
        }
        t=0;freq=0;
        for(i=0;i<rows;i++)
        {
            
            if(f[i]!=l[i]||f[0]!=f[i])
              t++;
            n=p[i];
            while(n!=0)
            {   d=n%10;
                if(d!=f[0])
                  freq++;
                n/=10;   }
            }
        if(t==0&&freq==0)
        {
            obj.AllSame(rows,f[0],p);
            
        }
        else
        {
        t=0;freq=0;
        for(i=0;i<rows;i++)
        {
            if(f[0]!=f[i])
             t++;
            if(l[0]!=l[i])
             freq++;
         }
        if(t==0)
        {
            obj.firstsame(rows,f,l,p);
        }
        else if(freq==0)
        {
          obj.lastsame(rows,f,l,p);
        }
        else
        {
          t=0;
          for(i=0;i<rows;i++)
          {
            num=p[i];a=num%10;
            while(num!=0)
            {
                d=num%10;
                if(d!=a)
                 t++;
                num/=10;
            }
          }
          if(t==0)
           obj.rowsame(rows,f,p);
         }
       }
    }
    void printclass()
    {
        System.out.println("public class Pattern\n{\npublic static void main()\n{\nint i,j;");
        //System.out.println("#include<stdio.h>\nvoid main()\n{\nint i,j;");
        }
    void printi(int s,int e,int up)
    {
        if(up>0)
        System.out.println("for(i="+s+";i<="+e+";i+="+up+")\n{");
        else
         System.out.println("for(i="+s+";i>="+e+";i-="+up*-1+")\n{");
        }
    void printj(int s,int e,int up)
    {
        if(up>0)
        {
          if(e==-1)
            System.out.println("for(j="+s+";j<=i;j+="+up+")\n{");
          else if(s==-1)
            System.out.println("for(j=i;j<="+e+";j+="+up+")\n{");
          else
            System.out.println("for(j="+s+";j<="+e+";j+="+up+")\n{");
            }
        else
        {
            if(e==-1)
              System.out.println("for(j="+s+";j>=i;j-="+up*-1+")\n{");
            else if(s==-1)
              System.out.println("for(j=i;j>="+e+";j-="+up*-1+")\n{");
            else
              System.out.println("for(j="+s+";j>="+e+";j-="+up*-1+")\n{");
            }
        }
    void printfinal(int t)
    {
        System.out.println("System.out.println(\""+t+"\");");
    }
    void rowsame(int rows,int f[],int p[])
    {
        int d=(p[1]%10)-(p[0]%10);
        int a=(p[1]+"").length()-(p[0]+"").length();
        printclass();
        System.out.println("int t="+(p[0]%10)+";");
        printi((p[0]+"").length(),(p[rows-1]+"").length(),a);
        printj(1,-1,1);
        //System.out.println("System.out.print(t);\n}\nSystem.out.println();");
        System.out.println("printf(\"%d\",t);\n}\nprintf(\"\n\");");
        if(d>0)
        System.out.println("t+="+d+";\n}\n}\n}");
        else
        System.out.println("t-="+(d*-1)+";\n}\n}\n}");
    }
    void firstsame(int rows,int f[],int l[],int p[])
    {
        int d;
        printclass();
        printi(l[0],l[rows-1],l[1]-l[0]);
        d=(p[rows-2]%10)-((p[rows-2]%100)/10);
        printj(f[0],-1,d);
        System.out.println("System.out.print(j);\n}\nSystem.out.println();\n}\n}\n}");
        //System.out.println("printf(\"%d\",j);\n}\nystem.out.println();\n}\n}\n}");
    }
    void lastsame(int rows,int f[],int l[],int p[])
    {
        int d;
        printclass();
        printi(f[0],f[rows-1],f[1]-f[0]);
        d=(p[rows-2]%10)-((p[rows-2]%100)/10);
        printj(-1,l[0],d);
        System.out.println("System.out.print(j);\n}\nSystem.out.println();\n}\n}\n}");
    }
    void AllSame(int rows,int t,int p[])
     {
       printclass();
          int a=(p[1]+"").length()-(p[0]+"").length();
          printi((p[0]+"").length(),(p[rows-1]+"").length(),a);
          printj(1,-1,1);
          printfinal(t);  
          System.out.println("}\nSystem.out.println();\n}\n}\n}");
    }
}
