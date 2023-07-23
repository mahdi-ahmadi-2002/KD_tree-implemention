# KD Tree Implementation

This repository contains a simple C++ implementation of a KD (K-Dimensional) tree, a data structure used for efficient searching in multidimensional spaces. The code defines functions to create, insert, search, and delete points in the KD tree.

## Usage

To use the KD tree, follow these steps:

1. Include the necessary header file:
```cpp
#include <bits/stdc++.h>
using namespace std;
```

2. Define the dimensionality of the points (in this case, k=2) and create a structure to represent a node in the KD tree.

3. Create a new KD tree node using the `newNode` function, passing the coordinates of the point.

4. Insert points into the KD tree using the `insert` function.

5. Search for points in the KD tree using the `search` function.

6. Delete points from the KD tree using the `deleteNode` function.

## Functions

### 1. `Node* newNode(int arr[])`

This function creates a new KD tree node with the given coordinates.

### 2. `Node* insert(Node* root, int point[])`

This function inserts a new point into the KD tree and returns the modified root of the tree.

### 3. `bool search(Node* root, int point[])`

This function searches for a point in the KD tree and returns `true` if the point is found, otherwise `false`.

### 4. `Node* deleteNode(Node* root, int point[])`

This function deletes a given point from the KD tree and returns the modified root of the tree.

### 5. `Node* findMin(Node* root, int d)`

This function finds the minimum point along the d'th dimension in the KD tree.

### 6. `Node* minNode(Node* x, Node* y, Node* z, int d)`

This function finds the node with the minimum value along the d'th dimension among the three given nodes.

### 7. `void copyPoint(int p1[], int p2[])`

This utility function copies the coordinates of one point into another.

## Example

```cpp
#include<bits/stdc++.h>
using namespace std;

// ... (Rest of the code, as provided)

int main()
{
    struct Node* root = NULL;
    int points[][k] = {{3, 6}, {17, 15}, {13, 15}, {6, 12},
                       {9, 1}, {2, 7}, {10, 19}};
    int n = sizeof(points)/sizeof(points[0]);

    // Inserting points into the KD tree
    for (int i=0; i<n; i++)
       root = insert(root, points[i]);

    // Searching for a point in the KD tree
    int searchPoint[k] = {6, 12};
    bool isFound = search(root, searchPoint);
    if (isFound)
        cout << "Point is present in the KD tree." << endl;
    else
        cout << "Point is not found in the KD tree." << endl;

    // Deleting a point from the KD tree
    int deletePoint[k] = {13, 15};
    root = deleteNode(root, deletePoint);

    return 0;
}
```

## Note

This is a simplified version of the KD tree implementation and may not be optimized for large datasets or real-world scenarios. Use it as a reference and consider further optimizations and error handling for your specific use case.
