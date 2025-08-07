# .NET-Backend-Interview-Questions

## C# Programming

1. **What are value types and reference types in C#?**

Value types are int, double, float, bool, char. These variables are usually stored in stack. These type of variables hold the exact value. When we assign one value type to a different    value type, then a new copy of the value gets assigned.
```
   public static void Main(string[] args)
{
    int k=2;
    int j = 4;
    k = j;
    k++;
    Console.WriteLine($"k: {k}, j: {j}");
    // k will be 5 and j will be 4, changing k does not impact j
}
```
By default value types will not have null value.

Reference types are string, class, struct, array
These types holds the memory reference to the actual data. By default, reference type does not point the object, so it is null. Referency types variable point the data present in the heap. When we assign reference type to a reference type, we assign the address of the value instead of the value it self.





   

