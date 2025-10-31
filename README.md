#Sum of Distinct Elements from Two Arrays

Algorithm SumDistinctElements
Input: array A[1..n], array B[1..m]
Output: integer sum

Var
    sum : integer         // To store the final sum of distinct elements
    i, j : integer        // Loop counters
    found : boolean       // Flag to check if element is found in the other array

Begin
    sum ← 0               // Initialize sum to 0

    // Loop through each element in array A
    For i ← 1 to n do
        found ← false     // Reset flag for each element
        // Check if A[i] exists in array B
        For j ← 1 to m do
            If A[i] = B[j] then
                found ← true
        EndFor
        // If A[i] is not found in B, add it to sum
        If found = false then
            sum ← sum + A[i]
    EndFor

    // Loop through each element in array B
    For i ← 1 to m do
        found ← false     // Reset flag for each element
        // Check if B[i] exists in array A
        For j ← 1 to n do
            If B[i] = A[j] then
                found ← true
        EndFor
        // If B[i] is not found in A, add it to sum
        If found = false then
            sum ← sum + B[i]
    EndFor

    Output sum            // Display the final result
End

#Dot Product and Othogonality Check
Procedure DotProduct(v1[1..k], v2[1..k], ps : out integer)
Var
    i : integer           // Loop counter
Begin
    ps ← 0                // Initialize dot product result
    // Loop through each component of the vectors
    For i ← 1 to k do
        ps ← ps + v1[i] * v2[i]   // Multiply and accumulate
    EndFor
End
