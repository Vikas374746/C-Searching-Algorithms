# EXPERIMENT NO – 20

* Aim: To study and implement searching techniques in C++ for finding elements in arrays.

* Tools Used: IDE, C++ compiler, arrays, functions, linear search, binary search.

* Theory:

In C++, searching is the process of locating a specific element within a data structure such as an array. It is an essential operation in programming to retrieve data efficiently.

-Searching helps in finding whether an element exists and its position in a collection.

-Different algorithms are used depending on whether the data is sorted or unsorted.

🔹 *Key Features of Searching:*

* Enables retrieval of data from arrays or other data structures.

* Supports both sorted and unsorted collections (depending on the method).

* Returns the index of the found element or indicates absence.

* Essential for applications requiring data lookup, filtering, or validation.

🔹 *Types of Searching in C++:*

i> Linear (Sequential) Search – Checks each element in order until the target is found.

*Syntax:*

    int linearSearch(int arr[], int size, int target) {
    for (int i = 0; i < size; i++) {
        if (arr[i] == target)
            return i;
    }
    return -1;
    }


ii> Binary Search – Efficient search on sorted arrays by repeatedly dividing the search interval in half.

*Syntax:*

    int binarySearch(int arr[], int size, int target) {
    int start = 0, end = size - 1;
    while (start <= end) {
        int mid = start + (end - start) / 2;
        if (arr[mid] == target)
            return mid;
        else if (arr[mid] < target)
            start = mid + 1;
        else
            end = mid - 1;
    }
    return -1;
    }


🔹 *Advantages of Searching:*

* Allows fast and efficient retrieval of elements.

* Essential for database queries, sorting, and algorithmic operations.

* Forms the foundation for more advanced search algorithms.

* Helps in validating and filtering data.


# Linear Search:

This program demonstrates how to search for a specific element in an array using the Linear Search method. The array is traversed sequentially from start to end, comparing each element with the target value until it is found or the array ends.

ALGORITHM:

1> Start

2> Declare and initialize array

* numbers[] = {10, 25, 30, 45, 50}

3> Define linearSearch function

* Loop i from 0 to size-1

* If arr[i] equals target, return i

*  If element not found, return -1

4> In main function

* Calculate size of array

* Call linearSearch with target element

* If index != -1, display "Target found at index"

* Else, display "Target not found"

5> End


# Binary Search:

This program demonstrates how to search for a specific element in a sorted array using the Binary Search method. The array is divided into halves repeatedly, and the middle element is compared with the target until the target is found or the sub-array size becomes zero.

ALGORITHM:

1> Start

2> Declare and initialize sorted array

* numbers[] = {10, 20, 30, 40, 50}

3> Define binarySearch function

* Initialize start = 0 and end = size-1

* While start ≤ end:

* Calculate middle = start + (end - start)/2

* If arr[middle] == target, return middle

* Else if arr[middle] < target, set start = middle + 1

* Else set end = middle - 1

* If element not found, return -1

4> In main function

* Calculate size of array

* Call binarySearch with target element

* If index != -1, display "Target found at index"

* Else, display "Target not found"

5> End


# Sequential Search:

This program demonstrates how to search for a specific element in an array using the Sequential Search method. The array is traversed one element at a time until the target is found or the end of the array is reached.

ALGORITHM:

1> Start

2> Declare and initialize array

* numbers[] = {5, 15, 25, 35, 45}

3> Define sequentialSearch function

* Initialize index = 0

* While index < size:

* If arr[index] == target, return index

* Increment index

* If element not found, return -1

4> In main function

* Calculate size of array

* Call sequentialSearch with target element

* If result != -1, display "Target found at index"

* Else, display "Target not found"

5> End



# Conclusion:

Searching implementation in C++ demonstrates how elements can be located in arrays effectively. Linear search is simple and works on any array, while binary search is faster for sorted arrays. Understanding these methods is fundamental for data handling and algorithm design.
