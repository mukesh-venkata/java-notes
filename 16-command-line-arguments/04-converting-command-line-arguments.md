<a name="top"></a>

# 🔄 4. Converting Command-Line Arguments

> **Core idea:** Command-line arguments arrive as Strings, so convert them when another data type is required.

## All Arguments Are Strings

Suppose we run:

~~~text
java Calculator 27
~~~

Then args[0] contains "27" as a String, not an int.

## Converting to int

Use Integer.parseInt():

~~~java
int age = Integer.parseInt(args[0]);
~~~

### Example

~~~java
public static void main(String[] args) {
    if (args.length > 0) {
        int number = Integer.parseInt(args[0]);
        System.out.println(number);
    }
}
~~~

## Other Common Conversions

| Required type | Conversion |
|---|---|
| int | Integer.parseInt(args[0]) |
| long | Long.parseLong(args[0]) |
| double | Double.parseDouble(args[0]) |
| float | Float.parseFloat(args[0]) |
| boolean | Boolean.parseBoolean(args[0]) |

## Invalid Numeric Input

If args[0] contains "abc" and we execute Integer.parseInt(args[0]), Java throws NumberFormatException because the text cannot be converted to an integer.

## Conversion Flow

~~~text
Command-line input
       ↓
String
       ↓
parse method
       ↓
required primitive type
~~~

Example:

~~~text
"27"
 ↓
Integer.parseInt()
 ↓
27
~~~

## Interview Questions

1. Are numeric command-line arguments automatically integers? No.
2. How do you convert a String argument to int? Integer.parseInt().
3. What happens if the text is not a valid integer? NumberFormatException can occur.
4. Can command-line arguments be converted to other types? Yes.

## Related Notes

- [Basics →](01-command-line-arguments-basics.md)
- [args Array →](02-args-array-and-accessing-arguments.md)
- [Running from Command Line →](03-running-from-command-line.md)
- [Quick Revision →](05-command-line-arguments-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)
