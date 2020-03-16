# 07-5 封裝-建構元的overloading

## 1. 範例
``` java
//-----------------------
// Score類別
//-----------------------
class Score{
    // 成員
    private int chi;
    private int eng;
    
    // 建構元(1)
    public Score(int chi, int eng) {
    	this.chi = chi;
    	this.eng = eng;
    }
    
    // 建構元(2)
    public Score() {}    
    
    // getter
    public int getChi() {return this.chi;}
    public int getEng() {return this.eng;}
    
    // setter
    public void setChi(int chi) {this.chi = chi;}
    public void setEng(int eng) {this.eng = eng;}
}

//-----------------------
// 一個名稱為J07_5的類別
//-----------------------
public class J07_5{

    public static void main(String []args){
        
        // 產生Score類別的實體s1, 並呼叫建構元
        Score s1 = new Score(80, 90);
    	
        // 印出實體s的成員
        System.out.println(s1.getChi());
        System.out.println(s1.getEng());   
        
        // 產生Score類別的實體s2, 並呼叫建構元
        Score s2 = new Score();
    	
        // 設定實體s2的成員值
        s2.setChi(75);
        s2.setEng(65);
        
        // 印出實體s2的成員
        System.out.println(s2.getChi());
        System.out.println(s2.getEng()); 
    }
}
``` 

## 2. 觀看教學影片
https://youtu.be/kWt_zQJXnXI


## 3. 完成以下練習


#### 3-1. 完成以下的程式

``` java
問題: 修改以上程式, 假設有第3個建構元, 它傳入1個參數, 並且將國文及英文都設定為參數值.
      例如, 傳入70, 則國文及英文都設定為70.
      請產生實體s3, 傳入1個參數值70, 寫入成員中, 再取出並印出成員值, 也印出總分及平均.
```
