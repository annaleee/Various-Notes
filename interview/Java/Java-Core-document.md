# Java Core Document

## String



## Arrays

`array.length`: length of array.  
`array = {1,2,3,4}`: initialize array.  
`Arrays.toString(array)`: convert array to a printable string.  
`Arrays.sort(array)`: sort the Array.  
`Arrays.parallelSort(array)`: sort the Array(Java 8).  
`Arrays.binarySearch(array, value: 2)`: the array must be sorted(Java 8).  
`Arrays.fill(array, fromidx:1, toidx:3, val:10)`: fill the array with value, not include toIdx.  
`Arrays.fill(array,val:10)`: fill the whole array with value.  

## List

`LinkedList<E> list = new LinkedList<E>();`.  
`list.add()`.  
`list.addFirst()`.  
`list.addLast()`.  
`list.removeFirst()`.  
`list.removeLast()`.  
`list.getFirst()`.  
`list.getLast()`.  
`list.get(2)`.  
`list.poll()`: delete and return the first element.  
`list.remove(2)`: if no index, then the same with poll.  
`list.contains()`.  
`list.indexOf()`: return the first index that element appear.  
`list.lastIndexOf()`.  
`list.peek()`: return the first element.  
`list.peekLast()`: return the last element.  
`list.set(idx,element)`.  
`list.toArray()`.  

## Set

`Set<String> hashSet = new HashSet<String>();`.  
`hashSet.add()`.  
`hashSet.size()`.  
`hashSet.contains()`.  
`hashSet.remove()`.  


```java
for(String str:hashSet){
    if(" ".equals(str)){
        boolean = "yes";
    }
}
```

## Hashmap

`HashMap<Integer, String> Sites = new HashMap<Integer, String>();`: initialize a hashmap.  
`Sites.put(1, "Google")`: put a new key-value.  
`Sites.clear();`.  
`Sites.size()`.  
`Sites.isEmpty()`.  
`Sites.putIfAbsent()`: insert a key-value if it is absent.  
`Sites.remove()`: remove an element according to the key.  
`Sites.containsKey()`: whether have key.  
`Sites.containsValue()`: whether have value.  
`Sites.replace()`: replace specific key.  
`Sites.replaceAll((key, value) -> value.toUpperCase());`: replace all of the key according to the function.  
`Sites.get()`.  
`Sites.getOrDefault()`.  
`int returnedValue = prices.merge("Shirt", 100, (oldValue, newValue) -> oldValue + newValue);`: if not exist, then add, if exist, then add according to the function.  
how to 遍历

```java
prices.forEach((key, value) -> {
            // value 价格减少百分之 10
            value = value - value * 10/100;
            System.out.print(key + "=" + value + " ");
        });
        
```

```java
for(Map.Entry<Integer, Integer> entry: map.entrySet()) {
    int key = entry.getKey();
    int value = entry.getValue();
}
```

```java
for(Integer key : map.keySet()){
    int key1 = key;
}
for(Integer val : map.values()){
    int value = val;
}
```

```java
Iterator<Map.Entry<Integer, INteger>> entries = map.entrySet().iterator();
while(entries.hasNext()){
    Map.Entry<Integer, Integer> entry = entries.Next();
}
```
