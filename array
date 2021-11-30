package com.company;

import java.util.Scanner;

public class Array {
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        int n=s.nextInt();
        int arr[]=new int[n];
        for(int i=0;i<n;i++){
             arr[i]=s.nextInt();
        }
        int sum=0;
        for(int i=0;i<n;i++){
            sum=arr[i]+sum;
        }
//        System.out.println(sum);
        int arr2[]=new int[n];
        for(int i=0;i<n;i++){
            arr2[i]=sum-arr[i];
        }
        for(int i=0;i<n;i++){
            System.out.print(arr2[i]+"  ");
        }
    }

}
