# 1.WAP to sort the given array in ascending and descending order.
```
#include <stdio.h>

int main() {
    int n, i, j, temp, arr[100];

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    printf("Enter the elements:\n");
    for(i = 0; i < n; i++)
        scanf("%d", &arr[i]);
    
    // Ascending Order
    for(i = 0; i < n - 1; i++) {
        for(j = i + 1; j < n; j++) {
            if(arr[i] > arr[j]) {
                temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
    }
    printf("Array in Ascending Order:\n");
    for(i = 0; i < n; i++)
        printf("%d ", arr[i]);
    printf("\n");

    // Descending Order
    for(i = 0; i < n - 1; i++) {
        for(j = i + 1; j < n; j++) {
            if(arr[i] < arr[j]) {
                temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
    }
    printf("Array in Descending Order:\n");
    for(i = 0; i < n; i++)
        printf("%d ", arr[i]);
    printf("\n");

    return 0;
}
```
## Output
```
Enter the number of elements: 5
Enter the elements:
9 8 7 6 5
Array in Ascending Order:
5 6 7 8 9 
Array in Descending Order:
9 8 7 6 5
```
# 2.Write a program to swap two numbers using function.
```
#include <stdio.h>

// Function to swap two numbers
void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    int x, y;
    printf("Enter two numbers: ");
    scanf("%d %d", &x, &y);

    printf("Before swapping: x = %d, y = %d\n", x, y);
    swap(&x, &y); // Pass addresses of x and y
    printf("After swapping: x = %d, y = %d\n", x, y);

    return 0;
}
```
## Output 
```
Enter two numbers: 2
23
Before swapping: x = 2, y = 23
After swapping: x = 23, y = 2
```
# 3.WAP to find minimum and maximum elements in a given array using the function intfind_max_min(int array[], int size, int *max, int *min);
```
#include <stdio.h>

// Function returns 0 on success
int find_max_min(int array[], int size, int *max, int *min) {
    if (size <= 0) {
        return -1; // error: empty array
    }

    *max = array[0];
    *min = array[0];

    for (int i = 1; i < size; i++) {
        if (array[i] > *max) {
            *max = array[i];
        }
        if (array[i] < *min) {
            *min = array[i];
        }
    }
    return 0; // success
}

int main() {
    int arr[100], n, max, min;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    if (find_max_min(arr, n, &max, &min) == 0) {
        printf("Maximum element = %d\n", max);
        printf("Minimum element = %d\n", min);
    } else {
        printf("Array is empty.\n");
    }

    return 0;
}
```
## Output
```
Enter the number of elements: 5
Enter 5 elements:
6
3
8
5
2
Maximum element = 8
Minimum element = 2
```
# 4.
