# CP-template-in-java

```
import java.io.*;
import java.util.*;

public class Main {
    public static class Task {
        public void solve(Scanner sc, PrintWriter pw) {
            int n = sc.nextInt();
            pw.println(n);
        }
    }

    public static void main(String... args) throws IOException {
        long startTime = System.nanoTime();
        Scanner sc;
        PrintWriter pw;
        if (System.getProperty("ONLINE_JUDGE") == null) {
          // Input is a file
            BufferedReader br = new BufferedReader(new FileReader(System.getenv("INPUT")));
            sc = new Scanner(br);
            pw = new PrintWriter(new BufferedWriter(new FileWriter(System.getenv("OUTPUT"))));
        } else {
          // Input is System.in
            sc = new Scanner(System.in);
            pw = new PrintWriter(new BufferedOutputStream(System.out));
        }
        
        
        
        
        Task t = new Task();
        int T = sc.nextInt();
        while (T-- > 0)
            t.solve(sc, pw);
        
        pw.close();

        long endTime = System.nanoTime();
        double durationMs = (endTime - startTime) / 1_000_000.0;
        System.err.println("Execution time: " + durationMs + " ms");
    }
}
```
