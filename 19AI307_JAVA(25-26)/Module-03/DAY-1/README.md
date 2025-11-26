# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

finalPrice = purchaseWeight * (goldRatePerGram - discount)

For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).

import java.util.Scanner;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
     
    }
}

//Continue your Code here

## AIM:
To write a Java program using inheritance and method overriding to calculate gold purchase price for different customer types (General, Regular, Premium) with discounts and cashback (for Premium customers).

## ALGORITHM :

1.Create a base class Customer with details and methods for discount and final price.

2.Create RegularCustomer and PremiumCustomer classes extending Customer.

3.Override getDiscountRate() and calculateFinalPrice() in derived classes.

4.Add cashback calculation in PremiumCustomer.

5.Read customer details from the user.

6.Create the appropriate customer object based on type.

7.Call the display() method to show results.



## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179 
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Genral");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer{
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram){
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }
    
    double getDiscountRate(){
        return 2;
    }
    
    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }
    
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer{
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram){
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }
    
    double getDiscountRate(){
        return 5;
    }
    
    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }
    
    double calculateCashback(){
        return calculateFinalPrice() * 0.01;
    }
    
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(calculateCashback()));
    }
}

class prog{
    public static void main(String[] main){
        Scanner sc = new Scanner(System.in);
        String type = sc.next();
        String id = sc.next();
        String name = sc.next();
        double pw = sc.nextDouble();
        double rate = sc.nextDouble();
        
        if(type.equals("Regular")){
            RegularCustomer r = new RegularCustomer(id, name, pw, rate);
            r.display();
        }
        else{
            PremiumCustomer p = new PremiumCustomer(id, name, pw, rate);
            p.display();
        }
    }
}
```


## OUTPUT:

<img width="860" height="752" alt="image" src="https://github.com/user-attachments/assets/1645f46c-e543-48a8-af24-182ec76477dd" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.
