package com.company;

interface Bank1 {
    float rateofinteresrt();
}
class SB1 implements Bank1{
    @Override
    public float rateofinteresrt() {
        return 9.5f;
    }
}
class PN1 implements Bank1{
    @Override
    public float rateofinteresrt() {
        return 8.5f;
    }
}
class Eeg{
    public static void main(String[] args) {
        Bank1 b;
        b=new SB1();
        System.out.println(b.rateofinteresrt());
        b=new PN1();
        System.out.println(b.rateofinteresrt());
    }
}
