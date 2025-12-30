# ASSIGNMENT


Program 1: Power Calculation
#include <stdio.h>
long long power(int a, int n) 
{
    long long result = 1;
    for(int i = 0; i < n; i++) 
    {
        result *= a;
    }
    return result;
}
int main()
{
    int a, n;
    printf("Enter base (a): ");
    scanf("%d", &a);
    printf("Enter exponent (n): ");
    scanf("%d", &n);
    printf("%d^%d = %lld\n", a, n, power(a, n));
    return 0;
}

Program 2: Sum of Digits
#include <stdio.h>
int sumOfDigits(int num)
{
    int sum = 0;
    while(num != 0)
    {
        sum += num % 10;
        num /= 10;
    }
    return sum;
}
int main() 
{
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    printf("Sum of digits: %d\n", sumOfDigits(num));
    return 0;
}

Program 3: Prime Check

#include <stdio.h>
#include <math.h>
int isPrime(int num) 
{
    if(num <= 1) 
    return 0;
    for(int i = 2; i <= sqrt(num); i++) 
    {
        if(num % i == 0) return 0;
    }
    return 1;
}
int main()
{
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    if(isPrime(num))
    {
        printf("%d is prime\n", num);
        }
    else
    {
        printf("%d is not prime\n", num);
        }
    return 0;
}

Program 4: GCD/HCF

#include <stdio.h>
int gcd(int a, int b) 
{
    int temp;
    while(b != 0) 
    {
        temp = b;
        b = a % b;
        a = temp;
    }
    return a;
}
int main()
{
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    printf("GCD of %d and %d is %d\n", a, b, gcd(a, b));
    return 0;
}

Program 5: Factorial (Recursive)

#include <stdio.h>
long long factorial(int n)
{
    if(n == 0 || n == 1)
    return 1;
    return n * factorial(n - 1);
}
int main()
{
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    printf("Factorial of %d is %lld\n", n, factorial(n));
    return 0;
}

Program 6: Read & Display Array (For Loop)

#include <stdio.h>
void readDisplayArrayFor(int arr[], int size) 
{
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++)
    {
        scanf("%d", &arr[i]);
    }
    printf("Array elements: ");
    for(int i = 0; i < size; i++)
    {
        printf("%d ", arr[i]);
    }
    printf("\n");
}
int main() {
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    readDisplayArrayFor(arr, size);
    return 0;
}

Program 7: Read & Display Array (While Loop)

#include <stdio.h>
void readDisplayArrayWhile(int arr[], int size)
{
    printf("Enter %d elements:\n", size);
    int i = 0;
    while(i < size) 
    {
        scanf("%d", &arr[i]);
        i++;
    }
    printf("Array elements: ");
    i = 0;
    while(i < size) 
    {
        printf("%d ", arr[i]);
        i++;
    }
    printf("\n");
}
int main()
{
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    readDisplayArrayWhile(arr, size);
    return 0;
}

Program 8: Sum of Array (For Loop)

#include <stdio.h>
int sumArrayFor(int arr[], int size)
{
    int sum = 0;
    for(int i = 0; i < size; i++)
    {
        sum += arr[i];
    }
    return sum;
}
int main()
{
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++)
    {
        scanf("%d", &arr[i]);
    }
    printf("Sum of array elements: %d\n", sumArrayFor(arr, size));
    return 0;
}

Program 9: Sum of Array (While Loop)

#include <stdio.h>
int sumArrayWhile(int arr[], int size)
{
    int sum = 0, i = 0;
    while(i < size)
    {
        sum += arr[i];
        i++;
    }
    return sum;
}
int main() {
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    int i = 0;
    while(i < size) 
    {
        scanf("%d", &arr[i]);
        i++;
    }
    printf("Sum of array elements: %d\n", sumArrayWhile(arr, size));
    return 0;
}

Program 10: Average of Array

#include <stdio.h>
float averageArray(int arr[], int size) 
{
    int sum = 0;
    for(int i = 0; i < size; i++) 
    {
        sum += arr[i];
    }
    return (float)sum / size;
}
int main() 
{
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++)
    {
        scanf("%d", &arr[i]);
    }
    printf("Average of array elements: %.2f\n", averageArray(arr, size));
    return 0;
}

Program 11: Sum of Elements Divisible by 3

#include <stdio.h>
int sumDivisibleBy3(int arr[], int size) 
{
    int sum = 0, i = 0;
    while(i < size)
    {
        if(arr[i] % 3 == 0)
        {
            sum += arr[i];
        }
        i++;
    }
    return sum;
}
int main()
{
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++) 
    {
        scanf("%d", &arr[i]);
    }
    printf("Sum of elements divisible by 3: %d\n", sumDivisibleBy3(arr, size));
    return 0;
}

Program 12: Count Even & Odd Numbers

#include <stdio.h>
void countEvenOdd(int arr[], int size, int *even, int *odd)
{
    *even = 0;
    *odd = 0;
    for(int i = 0; i < size; i++)
    {
        if(arr[i] % 2 == 0)
            (*even)++;
        else
            (*odd)++;
    }
}
int main()
{
    int size, even, odd;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++)
    {
        scanf("%d", &arr[i]);
    }
    countEvenOdd(arr, size, &even, &odd);
    printf("Even numbers: %d\n", even);
    printf("Odd numbers: %d\n", odd);
    return 0;
}

Program 13: Count Positive, Negative, Zero

#include <stdio.h>
void countPNZ(int arr[], int size, int *positive, int *negative, int *zero)
{
    *positive = 0;
    *negative = 0;
    *zero = 0;
    for(int i = 0; i < size; i++) 
    {
        if(arr[i] > 0)
            (*positive)++;
        else if(arr[i] < 0)
            (*negative)++;
        else
            (*zero)++;
    }
}
int main()
{
    int size, positive, negative, zero;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++)
    {
        scanf("%d", &arr[i]);
    }
    countPNZ(arr, size, &positive, &negative, &zero);
    printf("Positive numbers: %d\n", positive);
    printf("Negative numbers: %d\n", negative);
    printf("Zero numbers: %d\n", zero);
    return 0;
}

Program 14: Check Element Presence

#include <stdio.h>
int isElementPresent(int arr[], int size, int element) {
    for(int i = 0; i < size; i++) {
        if(arr[i] == element) {
            return 1;
        }
    }
    return 0;
}

int main() {
    int size, element;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++) {
        scanf("%d", &arr[i]);
    }
    
    printf("Enter element to search: ");
    scanf("%d", &element);
    
    if(isElementPresent(arr, size, element))
        printf("Element %d is present in the array\n", element);
    else
        printf("Element %d is NOT present in the array\n", element);
    return 0;
}
Program 15: Search Element with Positions
c
#include <stdio.h>

void searchAllPositions(int arr[], int size, int element) {
    int found = 0;
    printf("Element %d found at positions: ", element);
    for(int i = 0; i < size; i++) {
        if(arr[i] == element) {
            printf("%d ", i);
            found = 1;
        }
    }
    if(!found) {
        printf("Element not found in array");
    }
    printf("\n");
}

int main() {
    int size, element;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++) {
        scanf("%d", &arr[i]);
    }
    
    printf("Enter element to search: ");
    scanf("%d", &element);
    
    searchAllPositions(arr, size, element);
    return 0;
}
Program 16: Count Even Numbers
c
#include <stdio.h>

int countEvens(int arr[], int size) {
    int count = 0;
    for(int i = 0; i < size; i++) {
        if(arr[i] % 2 == 0) {
            count++;
        }
    }
    return count;
}

int main() {
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++) {
        scanf("%d", &arr[i]);
    }
    
    int evenCount = countEvens(arr, size);
    if(evenCount == 0)
        printf("No even numbers exist in the array\n");
    else
        printf("Number of even numbers: %d\n", evenCount);
    return 0;
}
Program 17: Find Maximum Element
c
#include <stdio.h>

int findMax(int arr[], int size) {
    int max = arr[0];
    for(int i = 1; i < size; i++) {
        if(arr[i] > max) {
            max = arr[i];
        }
    }
    return max;
}

int main() {
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++) {
        scanf("%d", &arr[i]);
    }
    
    printf("Maximum element: %d\n", findMax(arr, size));
    return 0;
}
Program 18: Find Max with Single Element Check
c
#include <stdio.h>

int findMaxWithCheck(int arr[], int size) {
    if(size == 1) {
        printf("Array has only one element\n");
        return arr[0];
    }
    
    int max = arr[0];
    for(int i = 1; i < size; i++) {
        if(arr[i] > max) {
            max = arr[i];
        }
    }
    return max;
}

int main() {
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++) {
        scanf("%d", &arr[i]);
    }
    
    printf("Maximum element: %d\n", findMaxWithCheck(arr, size));
    return 0;
}
Program 19: Find Second Largest
c
#include <stdio.h>
#include <limits.h>

int findSecondLargest(int arr[], int size) {
    if(size < 2) {
        printf("Array has less than 2 elements\n");
        return -1;
    }
    
    int first = INT_MIN, second = INT_MIN;
    int i = 0;
    while(i < size) {
        if(arr[i] > first) {
            second = first;
            first = arr[i];
        } else if(arr[i] > second && arr[i] != first) {
            second = arr[i];
        }
        i++;
    }
    
    if(second == INT_MIN) {
        printf("All elements are equal\n");
        return -1;
    }
    return second;
}

int main() {
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++) {
        scanf("%d", &arr[i]);
    }
    
    int secondLargest = findSecondLargest(arr, size);
    if(secondLargest != -1) {
        printf("Second largest element: %d\n", secondLargest);
    }
    return 0;
}
Program 20: Reverse Array
c
#include <stdio.h>

void reverseArray(int arr[], int size) {
    int reversed[size];
    for(int i = 0; i < size; i++) {
        reversed[i] = arr[size - 1 - i];
    }
    
    // Copy back to original array
    for(int i = 0; i < size; i++) {
        arr[i] = reversed[i];
    }
}

int main() {
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++) {
        scanf("%d", &arr[i]);
    }
    
    printf("Original array: ");
    for(int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
    
    reverseArray(arr, size);
    
    printf("Reversed array: ");
    for(int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
    return 0;
}
Program 21: Reverse Array In-Place
c
#include <stdio.h>

void reverseArrayInPlace(int arr[], int size) {
    int start = 0, end = size - 1;
    while(start < end) {
        // Swap elements
        int temp = arr[start];
        arr[start] = arr[end];
        arr[end] = temp;
        
        start++;
        end--;
    }
}

int main() {
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++) {
        scanf("%d", &arr[i]);
    }
    
    printf("Original array: ");
    for(int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
    
    reverseArrayInPlace(arr, size);
    
    printf("Reversed array: ");
    for(int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
    return 0;
}

Program 22: Reverse Array & Find Max

#include <stdio.h>
int reverseAndFindMax(int arr[], int size) 
{
    // Reverse the array
    for(int i = 0; i < size/2; i++)
    {
        int temp = arr[i];
        arr[i] = arr[size - 1 - i];
        arr[size - 1 - i] = temp;
    }
    int max = arr[0];
    for(int i = 1; i < size; i++) 
    {
        if(arr[i] > max)
        {
            max = arr[i];
        }
    }
    return max;
}
int main()
{
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++)
    {
        scanf("%d", &arr[i]);
    }
    printf("Original array: ");
    for(int i = 0; i < size; i++) 
    {
        printf("%d ", arr[i]);
    }
    printf("\n");
    int max = reverseAndFindMax(arr, size);
    printf("Reversed array: ");
    for(int i = 0; i < size; i++) 
    {
        printf("%d ", arr[i]);
    }
    printf("\n");
    printf("Maximum element: %d\n", max);
    return 0;
}

Program 23: Sort Array Ascending

#include <stdio.h>
void sortAscending(int arr[], int size) 
{
    for(int i = 0; i < size - 1; i++) 
    {
        for(int j = 0; j < size - i - 1; j++) 
        {
            if(arr[j] > arr[j + 1]) 
            {
                // Swap elements
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}
int main() 
{
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++)
    {
        scanf("%d", &arr[i]);
    }
    printf("Original array: ");
    for(int i = 0; i < size; i++)
    {
        printf("%d ", arr[i]);
    }
    printf("\n");
    sortAscending(arr, size);
    printf("Sorted array (ascending): ");
    for(int i = 0; i < size; i++)
    {
        printf("%d ", arr[i]);
    }
    printf("\n");
    return 0;
}

Program 24: Sort & Display Unique

#include <stdio.h>
void sortAndDisplayUnique(int arr[], int size) 
{
    for(int i = 0; i < size - 1; i++) 
    {
        for(int j = 0; j < size - i - 1; j++) 
        {
            if(arr[j] > arr[j + 1])
            {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
    printf("Unique elements: ");
    for(int i = 0; i < size; i++)
    {
        if(i > 0 && arr[i] == arr[i - 1])
        {
            continue;
        }
        printf("%d ", arr[i]);
    }
    printf("\n");
}
int main()
{
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++) 
    {
        scanf("%d", &arr[i]);
    }
    sortAndDisplayUnique(arr, size);
    return 0;
}

Program 25: Sort Array & Search Element

#include <stdio.h>
void sortAndSearch(int arr[], int size, int element) 
{
    for(int i = 0; i < size - 1; i++) {
        for(int j = 0; j < size - i - 1; j++) {
            if(arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
    printf("Sorted array: ");
    for(int i = 0; i < size; i++)
    {
        printf("%d ", arr[i]);
    }
    printf("\n");
    int found = 0;
    for(int i = 0; i < size; i++) {
        if(arr[i] == element) {
            printf("Element %d found at index %d in sorted array\n", element, i);
            found = 1;
            break;
        }
    }
    if(!found) 
    {
        printf("Element %d not found in the array\n", element);
    }
}
int main() 
{
    int size, element;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++)
    {
        scanf("%d", &arr[i]);
    }
    printf("Enter element to search: ");
    scanf("%d", &element);
    sortAndSearch(arr, size, element);
    return 0;
}

Program 26: Replace Negative with 0

#include <stdio.h>
void replaceNegativeWithZero(int arr[], int size)
{
    for(int i = 0; i < size; i++) 
    {
        if(arr[i] < 0)
        {
            arr[i] = 0;
        }
    }
}
int main() 
{
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++) 
    {
        scanf("%d", &arr[i]);
    }
    printf("Original array: ");
    for(int i = 0; i < size; i++) 
    {
        printf("%d ", arr[i]);
    }
    printf("\n");
    replaceNegativeWithZero(arr, size);
    printf("Modified array: ");
    for(int i = 0; i < size; i++) 
    {
        printf("%d ", arr[i]);
    }
    printf("\n");
    return 0;
}

Program 27: Swap First & Last Elements

#include <stdio.h>
void swapFirstLast(int arr[], int size) 
{
    if(size > 1)
    {
        int temp = arr[0];
        arr[0] = arr[size - 1];
        arr[size - 1] = temp;
    }
}
int main() 
{
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++)
    {
        scanf("%d", &arr[i]);
    }
    printf("Original array: ");
    for(int i = 0; i < size; i++)
    {
        printf("%d ", arr[i]);
    }
    printf("\n");
    swapFirstLast(arr, size);
    printf("Modified array: ");
    for(int i = 0; i < size; i++) 
    {
        printf("%d ", arr[i]);
    }
    printf("\n");
    return 0;
}

Program 28: Delete Element by Position

#include <stdio.h>
void deleteElement(int arr[], int *size, int position) 
{
    if(position < 0 || position >= *size)
    {
        printf("Invalid position!\n");
        return;
    }
    for(int i = position; i < *size - 1; i++)
    {
        arr[i] = arr[i + 1];
    }
    (*size)--;
}
int main() {
    int size, position;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++)
    {
        scanf("%d", &arr[i]);
    }
    printf("Enter position to delete (0 to %d): ", size - 1);
    scanf("%d", &position);
    deleteElement(arr, &size, position);
    printf("Modified array: ");
    for(int i = 0; i < size; i++)
    {
        printf("%d ", arr[i]);
    }
    printf("\n");
    return 0;
}

Program 29: Multiple Operations on Array

#include <stdio.h>
int sumArray(int arr[], int size) 
{
    int sum = 0;
    for(int i = 0; i < size; i++)
    {
        sum += arr[i];
    }
    return sum;
}
int findMax(int arr[], int size) {
    int max = arr[0];
    for(int i = 1; i < size; i++) {
        if(arr[i] > max) {
            max = arr[i];
        }
    }
    return max;
}
void countEvenOdd(int arr[], int size, int *even, int *odd) {
    *even = 0;
    *odd = 0;
    for(int i = 0; i < size; i++)
    {
        if(arr[i] % 2 == 0)
            (*even)++;
        else
            (*odd)++;
    }
}
int main()
{
    int size, even, odd;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++)
    {
        scanf("%d", &arr[i]);
    }
    printf("\nResults:\n");
    printf("Sum of array elements: %d\n", sumArray(arr, size));
    printf("Maximum element: %d\n", findMax(arr, size));
    countEvenOdd(arr, size, &even, &odd);
    printf("Even numbers: %d\n", even);
    printf("Odd numbers: %d\n", odd);
    return 0;
}

Program 30: Sum of Even & Product of Odd

#include <stdio.h>
int sumEvenElements(int arr[], int size) 
{
    int sum = 0;
    for(int i = 0; i < size; i++)
    {
        if(arr[i] % 2 == 0)
        {
            sum += arr[i];
        }
    }
    return sum;
}
long productOddElements(int arr[], int size)
{
    long product = 1;
    int hasOdd = 0;
    for(int i = 0; i < size; i++) 
    {
        if(arr[i] % 2 != 0)
        {
            product *= arr[i];
            hasOdd = 1;
        }
    }
    return hasOdd ? product : 0;
}
int main() {
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    for(int i = 0; i < size; i++) 
    {
        scanf("%d", &arr[i]);
    }
    printf("\nResults:\n");
    printf("Sum of even elements: %d\n", sumEvenElements(arr, size));
    long product = productOddElements(arr, size);
    if(product == 0) 
    {
        printf("No odd elements found\n");
    } else 
    {
        printf("Product of odd elements: %ld\n", product);
    }
    return 0;
}

Program 31: Multiple Operations with While Loop

#include <stdio.h>
int sumEvenNumbers(int arr[], int size)
{
    int sum = 0, i = 0;
    while(i < size)
    {
        if(arr[i] % 2 == 0)
        {
            sum += arr[i];
        }
        i++;
    }
    return sum;
}
int findMaximum(int arr[], int size)
{
    int max = arr[0], i = 1;
    while(i < size)
    {
        if(arr[i] > max) 
        {
            max = arr[i];
        }
        i++;
    }
    return max;
}
int searchElement(int arr[], int size, int element)
{
    int i = 0;
    while(i < size)
    {
        if(arr[i] == element) 
        {
            return i;
        }
        i++;
    }
    return -1;
}
void sortArray(int arr[], int size) 
{
    int i = 0;
    while(i < size - 1) 
    {
        int j = 0;
        while(j < size - i - 1)
        {
            if(arr[j] > arr[j + 1]) 
            {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
            j++;
        }
        i++;
    }
}
int main() 
{
    int size, element;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    int i = 0;
    while(i < size)
    {
        scanf("%d", &arr[i]);
        i++;
    }
    printf("Enter element to search: ");
    scanf("%d", &element);
    printf("\nResults:\n");
    printf("Sum of even numbers: %d\n", sumEvenNumbers(arr, size));
    printf("Maximum element: %d\n", findMaximum(arr, size));
    int pos = searchElement(arr, size, element);
    if(pos != -1)
        printf("Element %d found at index %d\n", element, pos);
    else
        printf("Element %d not found\n", element);
    sortArray(arr, size);
    printf("Sorted array: ");
    i = 0;
    while(i < size) 
    {
        printf("%d ", arr[i]);
        i++;
    }
    printf("\n");
    return 0;
}

Program 32: Multiple Operations with While Loop

#include <stdio.h>
int countEvenNumbers(int arr[], int size)
{
    int count = 0, i = 0;
    while(i < size)
    {
        if(arr[i] % 2 == 0)
        {
            count++;
        }
        i++;
    }
    return count;
}
void replaceOddWithZero(int arr[], int size) 
{
    int i = 0;
    while(i < size)
    {
        if(arr[i] % 2 != 0) 
        {
            arr[i] = 0;
        }
        i++;
    }
}
void displayArray(int arr[], int size)
{
    int i = 0;
    printf("Array elements: ");
    while(i < size) 
    {
        printf("%d ", arr[i]);
        i++;
    }
    printf("\n");
}
int main()
{
    int size;
    printf("Enter array size: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements:\n", size);
    int i = 0;
    while(i < size) 
    {
        scanf("%d", &arr[i]);
        i++;
    }
    printf("\nResults:\n");
    printf("Count of even numbers: %d\n", countEvenNumbers(arr, size));
    replaceOddWithZero(arr, size);
    displayArray(arr, size);
    return 0;
}
