## Quiz_Gift
**Java:**
```java
import java.util.Scanner;

public class Main {
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        int[] cnt = new int[110];
	int mx = -1;
        int n = sc.nextInt();
        int m = sc.nextInt();
        for(int i=1;i<=m;i++){
            int num = sc.nextInt();
            cnt[num%n]++;
            mx = Math.max(mx,cnt[num%n]);
        }
        for(int i=0;i<n;i++)
            if(cnt[i] == mx){
                System.out.print(i + " ");
            }
        System.out.println("");
        mx = 0;
        for(int i=0;i<n;i++)
            if(cnt[i] == 0){
                System.out.print(i + " ");
                mx = 1;
            }
        if(mx == 0){
            System.out.print("Everyone recieve the gifts.");
        }
    }
}
```
