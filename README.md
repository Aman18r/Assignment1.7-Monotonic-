# Assignment1.7-Monotonic-

import java.io.*;
public class Main{
    static boolean check(int arr[]){
        int n = arr.length;
        boolean inc = true;
        boolean dec = true;

        for(int i = 0; i < n-1; i++){
            if(arr[i] > arr[i + 1]){
                inc = false;
            }
        }
        for(int i = 0; i < n-1; i++){
            if(arr[i] < arr[i + 1]){
                dec = false;
            }
        }
        return inc || dec;
    }

    public static void main(String[] args) {
        int arr[] = {1,2,2,3};

        boolean ans = check(arr);
        if(ans == true)
            System.out.println("Yes");
        else
            System.out.println("No");

    }
}
