# shardul-dsa-
1) Functions in C and Arrays
   C program with a function that reverses an array.
   #include <stdio.h>
void reverseArray(int arr[], int n) {   //in this we use this function to reverse the array using while loop 
    int start = 0, end = n - 1;
    while (start < end) {
        int temp = arr[start];
        arr[start] = arr[end];
        arr[end] = temp;
        start++;
        end--;
    }
}

void printArray(int arr[], int n) {     //in this we declare the fuction for printing the arrays
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}

int main() {
    int arr[] = {1, 2, 3, 4, 5};
    int n = sizeof(arr) / sizeof(arr[0]);

    printf("Original Array: ");
    printArray(arr, n);  // calling printarray function

    reverseArray(arr, n);  //in this main function call the reverse function

    printf("Reversed Array: ");
    printArray(arr, n);

    return 0;
}

   
