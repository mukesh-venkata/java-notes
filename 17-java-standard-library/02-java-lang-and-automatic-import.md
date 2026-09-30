<a name="top"></a>

# 📦 2. java.lang & Automatic Import

> **Core idea:** The `java.lang` package is automatically available to every Java source file.

## 🧠 What Is java.lang?

`java.lang` contains many fundamental Java classes, including:

- `String`
- `System`
- `Math`
- `Object`
- `Integer`

Because `java.lang` is automatically imported, you normally do not need to write explicit imports for these types.

## Example

This works without an import:

~~~java
public class Demo {
    public static void main(String[] args) {
        String name = "Java";
        System.out.println(name);
        System.out.println(Math.max(10, 20));
    }
}
~~~

You do **not** normally need:

~~~java
import java.lang.String;
~~~

## 🔄 What Does “Automatically Imported” Mean?

Conceptually, the compiler makes the types in `java.lang` available without requiring an explicit import declaration.

It does **not** mean every class from every Java package is automatically imported.

For example, `ArrayList` is in `java.util`, so you normally import it:

~~~java
import java.util.ArrayList;
~~~

## 📌 Important Points

- `java.lang` is automatically available.
- `String`, `System`, `Math`, `Object`, and `Integer` are examples.
- You normally do not write explicit `java.lang` imports.
- Other packages such as `java.util` are not automatically imported.

## 🎯 Interview Questions

### Q1. Which Java package is automatically imported?
`java.lang`.

### Q2. Is `String` in `java.lang`?
Yes.

### Q3. Do we normally write `import java.lang.String;`?
No.

### Q4. Is `java.util` automatically imported?
No.

## 🔗 Related Notes

- [Library Overview →](01-java-standard-library-overview.md)
- [String & length() →](03-string-and-length.md)
- [Commonly Used Packages →](04-commonly-used-java-packages.md)
- [Quick Revision →](05-java-standard-library-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)
