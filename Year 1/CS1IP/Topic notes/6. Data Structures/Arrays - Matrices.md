#CS1IP
## 2 Dimensional Arrays
- A 2 dimensional [[Arrays|array]] is a way of describing an 'array of arrays' -> another way of describing a **matrix**:
```Java
int[][] matrix1 = new int [3][3]; //3 x 3 matrix
matrix [0][0] = 1; //Initialises a value (top left corner)

int [][] matrix2 = {
	{1, 2, 3},
	{4, 5, 6},
	{7, 8, 9}
}; //Initialised upon declaration/allocation
```
- Iterating through a 2D array is similar to iterating through a standard array but requires a nested loop too; one handles `i`, the other `j`.
```Java
for(int i = 0; i <3; i++) {
	for(int j = 0; j < 3; j++) {
		System.out.print(matrix2[i][j] + " ");
	}
	System.out.println();
}
```
- print is used inside the inner loop to `print()` elements on the same line, while `println()` is used in the outer loop to separate the matrix into 3 rows
- Alternatively, you can use a `for-each` loop:
```Java
int[][] matrix {
	{1, 2, 3},
	{4, 5, 6},
	{7, 8, 9},
};
for(int[] row : matrix) {
	for(int element : row) {
		System.out.print(element + " ");
	}
	System.out.println();
}
```
## Identity Matrix
- An identity matrix is a square matrix where all diagonal elements are 1, and the rest are 0
```Java
int[][] matrix {
	{1, 0, 0},
	{0, 1, 0},
	{0, 0, 1},
};
```
## Determinant of a 2x2 Matrix
The determinant of a 2 x 2 matrix is calculated by subtracting the product of the diagonals: `det(A) = (a00 * a11) - (a01 * a10)`:
```Java
int[][] matrix = {
	{4, 3},
	{6, 3},
};
int det = (matrix[0][0] * matrix[1][1]) - (matrix[0][1] * matrix[1][0]);
//Output = -6
```
## Transpose
The transpose of a matrix is when you swap the rows and columns:
```
int[][] A = {
	{a11, a12, a13},
	{a21, a22, a23},
};

int[][] A^T = {
	{a11, a21},
	{a12, a22},
	{a13, a23},
}
```
## IndexOutOfBoundsException in Multidimensional Arrays
`IndexOutOfBoundsException` also applies to 2D arrays -> each dimension is bounds-checked separately. E.g. for a `new int[2][2]` (valid row/col indices: 0 and 1 only):
```java 
matrix[2][1] = 5; // IndexOutOfBoundsException — row index 2 doesn't exist
```
---
## Covered in
- [[CS1IP_week_05_lecture.pdf]]