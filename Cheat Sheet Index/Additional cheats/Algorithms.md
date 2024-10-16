Here's your **JavaScript Data Structures & Algorithms Cheat Sheet** cleaned up and formatted correctly in Markdown, following the same structure as the Redux Cheat Sheet you provided:

````markdown
# JavaScript Data Structures & Algorithms Cheat Sheet

## Data Structures

### Arrays

- **Definition**: An ordered collection of items, indexed by integers.
- **Common Methods**:
  - `push(element)`: Adds an element to the end.
  - `pop()`: Removes the last element.
  - `shift()`: Removes the first element.
  - `unshift(element)`: Adds an element to the beginning.
  - `slice(start, end)`: Returns a portion of the array.
  - `splice(start, deleteCount, items...)`: Adds/removes items.

---

### Linked Lists

- **Definition**: A collection of nodes, where each node contains data and a reference to the next node.
- **Node Structure**:
  ```javascript
  class Node {
      constructor(data) {
          this.data = data;
          this.next = null;
      }
  }
  ```
````

- **Common Operations**:
  - **Insert**: Add a node.
  - **Delete**: Remove a node.
  - **Search**: Find a node.

---

### Stacks

- **Definition**: A collection of elements that follows Last In First Out (LIFO).
- **Methods**:
  - `push(element)`: Adds an element to the top.
  - `pop()`: Removes the top element.
  - `peek()`: Returns the top element without removing it.

---

### Queues

- **Definition**: A collection of elements that follows First In First Out (FIFO).
- **Methods**:
  - `enqueue(element)`: Adds an element to the end.
  - `dequeue()`: Removes the front element.
  - `peek()`: Returns the front element without removing it.

---

### Trees

- **Definition**: A hierarchical structure with a root value and subtrees of children.
- **Binary Tree**: Each node has at most two children.
- **Binary Search Tree (BST)**: Left child < Parent < Right child.

---

### Hash Tables

- **Definition**: A collection of key-value pairs with fast access to values based on keys.
- **Common Methods**:
  - `set(key, value)`: Adds or updates a value.
  - `get(key)`: Retrieves a value.
  - `delete(key)`: Removes a key-value pair.

---

## Algorithms

### Sorting Algorithms

1. **Bubble Sort**: Repeatedly swaps adjacent elements if they are in the wrong order.

   ```javascript
   function bubbleSort(arr) {
       for (let i = 0; i < arr.length; i++) {
           for (let j = 0; j < arr.length - i - 1; j++) {
               if (arr[j] > arr[j + 1]) {
                   [arr[j], arr[j + 1]] = [arr[j + 1], arr[j]];
               }
           }
       }
       return arr;
   }
   ```

2. **Selection Sort**: Finds the smallest element and swaps it with the first unsorted element.

   ```javascript
   function selectionSort(arr) {
       for (let i = 0; i < arr.length; i++) {
           let minIndex = i;
           for (let j = i + 1; j < arr.length; j++) {
               if (arr[j] < arr[minIndex]) {
                   minIndex = j;
               }
           }
           [arr[i], arr[minIndex]] = [arr[minIndex], arr[i]];
       }
       return arr;
   }
   ```

3. **Insertion Sort**: Builds a sorted array one element at a time.

   ```javascript
   function insertionSort(arr) {
       for (let i = 1; i < arr.length; i++) {
           let key = arr[i];
           let j = i - 1;
           while (j >= 0 && arr[j] > key) {
               arr[j + 1] = arr[j];
               j--;
           }
           arr[j + 1] = key;
       }
       return arr;
   }
   ```

4. **Quick Sort**: Divides the array into smaller sub-arrays, sorts them, and combines them.

   ```javascript
   function quickSort(arr) {
       if (arr.length <= 1) return arr;
       const pivot = arr[arr.length - 1];
       const left = arr.filter(x => x < pivot);
       const right = arr.filter(x => x > pivot);
       return [...quickSort(left), pivot, ...quickSort(right)];
   }
   ```

---

### Searching Algorithms

1. **Linear Search**: Checks each element until the desired element is found.

   ```javascript
   function linearSearch(arr, target) {
       for (let i = 0; i < arr.length; i++) {
           if (arr[i] === target) return i;
       }
       return -1;
   }
   ```

2. **Binary Search**: Searches a sorted array by repeatedly dividing the search interval in half.

   ```javascript
   function binarySearch(arr, target) {
       let left = 0;
       let right = arr.length - 1;
       while (left <= right) {
           const mid = Math.floor((left + right) / 2);
           if (arr[mid] === target) return mid;
           if (arr[mid] < target) left = mid + 1;
           else right = mid - 1;
       }
       return -1;
   }
   ```

---

```

```
