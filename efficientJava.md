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
Note:

This is only for primitive array.

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

### 3. Arithmetic Calculation
Bad
```java
float a = (x * x - y * y) / (x * x + y * y);
float b = (x * x * y - y * y * x) / (x * x + y * y);
```

Good
```java
float c = 1f / (x * x + y * y);
float d = x - y;
float a = (x + y) * d * c;
float b = x * y * d * c;
```

Note:

Speed : ADD ~ SUB > MULT > DIV

### 4. Autoboxing/Unboxing
Bad
```java
public interface Calculation<V> {
  V getValue();
  void calc(Calculation<V> value);
}
public class Test implements Calculation<Float> {
  private float value;
  public Float getValue() {
    return this.value;
  }
  public void calc(Calculation<Float> value) {
    this.value = value.getValue() * value.getValue() * value.getValue();
  }
}
```
Good
```java
public class Test... {
  public void calc(Calculation<Float> value) {
     Test temp = (Test)value;
     this.value = temp.value * temp.value * temp.value; 
  }
}
```
Note:

Autoboxing/Unboxing are useful for coding. But they will be a factor for bad performance.
