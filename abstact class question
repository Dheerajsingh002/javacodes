package com.company;

abstract class Bank {
    abstract int rateofinterest();
}
class SBI extends Bank{
    @Override
    int rateofinterest() {
        return 7;
    }
}
class PNB extends Bank{
    @Override
    int rateofinterest() {
        return 9;
    }
}
class Abc{
    public static void main(String[] args) {
       Bank b;
       b=new SBI();
        System.out.println(b.rateofinterest());
        b=new PNB();
        System.out.println(b.rateofinterest());
    }
}
