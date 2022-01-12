public class Main {

    /**
     * @param args
     */
    public static void main(String[] args) {
        // TODO Auto-generated method stub
        division(7); //This method is a test example to show how the function works


    }

    public static void division(int n){ //this method generate all numbers multiple of a particular one and get the first one who is constitute by 1s or/and 0s
        boolean x=false;
        int j=2;
        do {
            for (int i=1;i<j;i++){
                if (i%n==0&&check(i).equalsIgnoreCase("correct")){
                    System.out.println("The correct multiple is: "+i);
                    x=true;
                }else {
                    x=false;
                    j=j+1;
                }
            }
        }while (x==false);
    }

    public static String check(int a){ //that function check if a string is constitute by 0s or/and 1s
        String status ="";
        String s =Integer.toString(a) ;
        for (int z = 0; z < s.length(); z++) {
            if( "0".equals(Character.toString(s.charAt(0)))||"1".equals(Character.toString(s.charAt(0))) )
            {
                if(Character.toString(s.charAt(z)).equals("0")||Character.toString(s.charAt(z)).equals("1") ){
                  status ="correct";
                }else{
                  return status ="incorrect";
                }
            }
            else{
              return status ="incorrect";
            }
        }
        return status;
    }
}
