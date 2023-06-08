# ALIŞTIRMA :
* 1'den 999'a kadarki hangi sayının armstrong sayı olup olmadığını ekrana yazdırma
```
public class deneme {
    public static void main(String[] args){
        for (int i=1;i<=999;i++){
            System.out.println(i);
            int busNumber=0;
            int tempNumber;
            int busValue;
            int result=0;
            int busPow;
            tempNumber=i;
            while (tempNumber!=0){
                tempNumber/=10;
                busNumber++;
            }

            tempNumber=i;

            while (tempNumber!=0){
                busValue=tempNumber%10;
                busPow=1;
                for (int j=1;j<=busNumber;j++){
                    busPow*=busValue;
                }
                result+=busPow;
                tempNumber/=10;
            }
            if (i==result){
                System.out.println(i+" Sayısı bir armstrong sayıdır");
            }else{
                System.out.println(i+" Sayısı bir armstrong sayı değildir");
            }
        }
    }
}
```