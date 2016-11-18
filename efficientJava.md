# Efficient Programming for Java

## Anti pattern

### 1. Array Copy
Bad
```java
int[] newArray = new int[origin.length];
for (int i = 0; i < origin.length; i++) {
  newArray[i] = origin[i];
}
```

Good
```java
import java.util.Arrays;
int[] newArray = Arrays.copyOf(origin, origin.length);
```

### 2. Array Access with ``for``
Bad
```java
for (int i = 0; i < array.length; i++) {
  array[i] = ...
}
```

Good
```java
for (int i = 0, n = array.length; i < n; i++) {
  array[i] = ...    
}
```
