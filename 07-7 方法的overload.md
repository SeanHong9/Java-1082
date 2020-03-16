# 07-7 方法的overload

## 1. 範例
``` java
//-----------------------
// Product類別
//-----------------------
class Product{
    // 成員
    private String title;
    private int price;
    
    // 建構元
    public Product(String title, int price) {
        this.title = title;
        this.price = price;
    }
    
    // getter
    public String getTitle() {return this.title;}
    public int getPrice() {return this.price;}
    
    // 計算消費稅的方法(1)
    public int tax(double rate) {
        return (int)(this.price * rate);
    }
    
    // 計算消費稅的方法(2)
    public int tax() {
        return (int)(this.price * 0.18);
    }    
}

//-----------------------
// 一個名稱為J08_2的類別
//-----------------------
public class J08_2{

    public static void main(String []args){
        
        // 產生Product類別的實體p1, 並呼叫建構元
        Product p1 = new Product("行李箱", 3500);
    	
        // 印出實體s的成員
        System.out.println(p1.getTitle());
        System.out.println(p1.getPrice());   
        
        // 印出稅金
        System.out.println(p1.tax(0.15));
        
        // 產生Product類別的實體p, 並呼叫建構元
        Product p2 = new Product("葯品", 2550);
    	
        // 印出實體s的成員
        System.out.println(p2.getTitle());
        System.out.println(p2.getPrice());   
        
        // 印出稅金
        System.out.println(p2.tax());        
    }
}
``` 

## 2. 觀看教學影片
https://youtu.be/qV2T2TjQJXM


## 3. 完成以下練習


#### 3-1. 完成以下的程式

``` java
問題: 修改以上程式, 增加1個方法：

      // 計算運費的方法(請自行完成)
      public int tax(boolean taxFree) {        
      }
      
      傳入1個參數, 意義是"是否免稅商品?", 費稅的計算如下: 
      如果是免稅商品, 回傳0;
      如果不是, 以0.18的消費稅率計算回傳消費稅.      
```
