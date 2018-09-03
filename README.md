# Largest-number-in-a-list
import java.util.Map;
import java.util.HashMap;
public class Example {
 public static void main(String[] args){
 int[] numbers=new int[]{1,2,3,2,2,2,1,4,3,1};
 System.out.println(methodOne(numbers));
 }
 public static int methodOne(int[] numbers){
 Map<Integer,Integer> map=new HashMap<>();
 
 for(int i=0; i<numbers.length; i++){
  if(map.containsKey(numbers[i]))map.put(numbers[i],map.get(numbers[i])+1);
  else map.put(numbers[i],1);
 }
 int highest=0;
 int best=0;
 for(Integer a:map.keySet()){
 if(map.get(a)>highest){
  highest=map.get(a);
  best=a;
  }
 }
 return best;
 }
}
