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
These types holds the memory reference to the actual data. By default, reference type does not point the object, so it is null. Reference types variable point the data present in the heap. When we assign reference type to a reference type, we assign the address of the value instead of the value it self.

2.  **What is the difference between '==' and '.Equals()'**?

== operator checks reference equality of reference type, where as .Equals() methods checks for the content equlity. But in case of C#, for string, == and .Equals() both compare the value instead of reference. Because String class has operator overloading for == which basically compares the value, and also String class overrides the .Equals() method to compare the value.
```
public static void Main(string[] args)
{
    string s = new string("sdss");
    string k = new string("sdss");

    Console.WriteLine(s==k);  // return true because of == operator overloading to compare values
    Console.WriteLine(s.Equals(k)); // return true because .Equals() is overridden in string to compare value

    object s1 = new string("sdss"); //return false because of object's == operator compare references
    object k1 = new string("sdss"); // returns true, at runtime both the objects gets converted to string type and .Equals() compares values for string

    Console.WriteLine(s1 == k1);
    Console.WriteLine(s1.Equals(k1));



}
```






   

