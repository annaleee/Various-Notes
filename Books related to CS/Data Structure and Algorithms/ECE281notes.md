[toc]

## Algorithm Analysis

## Sorting

### Insertion Sort

* 从0到N-1，把每一个数都插进前面的正确的顺序里
* Time complexity: O(N^2)
* Place complexity: O(1)
* Stable
* Best case: O(N)
* Worst case: O(N^2)

### Selection Sort

* 从i到N-1,寻找后面几个最小的数字
* Time complexity: O(N^2)

### Bubble Sort

* 从倒数第二个到0，j从0到i，两两相邻的数进行交换

* ```C++
  for(i = N-2; i>=0; i--){
  	for(j = 0; j<=i;j++){
  		if(A[j]>A[j+1]){
  			swap(A[j],A[j+1]);
  		}
  	}
  }
  ```

* Time Complexity: O(N^2)

* In place? Yes

* Stable

### Merge Sort

* 把很多数拆成一个一个，然后再逐渐merge进去

* ```C++
  void mergesort(int *a, int left, int right){
    	if(left >= right) return;
    	int mid = (left+right)/2;
    	mergesort(a, left, mid);
    	mergesort(a, mid+1, right);
    	merge(a, left, mid, right);
  }
  ```

* Time Complexity: O(nlogn)

### Quick Sort

* 选一个数作为中点，把所有比他小的放一边。比他大的放另一边

* ```C++
  void quicksort(int *a, int left, int right){
    	int pivotat;
    	if(left <= right) return;
    	pivotat = partition(a, left, right);
    	quicksort(a, left, pivotat - 1);
    	quicksort(a, pivotat + 1,right);
  }
  ```

* O(nlogn)

## Hash Function

### Hashing Basic

