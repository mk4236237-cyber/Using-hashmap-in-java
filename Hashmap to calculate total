import java.io.File;
import java.util.Scanner;
import java.util.HashMap;
public class UsingHashmap {
    public static void main(String[] args) throws Exception{
      Scanner inp=new Scanner(System.in);
      System.out.println("Enter file: ");
      String file=inp.nextLine();
  HashMap<String, Integer> map= new HashMap<>();
  File f=new File(file);
  Scanner sc=new Scanner(f);
  if (sc.hasNextLine()) sc.nextLine();
  while (sc.hasNextLine()){
    String line= sc.nextLine().trim();
    if(line.isEmpty()) continue;
    String[] parts=line.split("\\s+");
    if(parts.length>=5){
        String product = parts[3];
        int amount= Integer.parseInt(parts[4]);
        if(map.containsKey(product)){
          int oldamount= map.get(product);
            map.put(product, oldamount +amount);
        }
        else{
            map.put(product, amount);
        }
    }
  }
  sc.close();
  int gtotal=0;
  System.out.println("Product Wise Total:");
  for(String product : map.keySet()){
    int total =map.get(product);
    System.out.println(product +" :" + total);
    gtotal += total;
  }
  System.out.println("Grand Total of all products : " + gtotal);
  }
 }
