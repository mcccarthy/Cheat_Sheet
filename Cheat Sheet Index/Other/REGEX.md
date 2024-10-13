# Regex Cheat Sheet

## 1. **Common Regex Patterns**

| Pattern                      | Description                                    | Example Match                     |
|------------------------------|------------------------------------------------|-----------------------------------|
| `^abc`                       | Starts with "abc".                            | "abc123", "abc"                   |
| `abc$`                       | Ends with "abc".                              | "123abc", "abc"                   |
| `a.b`                       | Matches "a", any character, "b".              | "acb", "a1b", "a b"               |
| `a*b`                       | Matches "a" zero or more times followed by "b". | "b", "ab", "aaab"                 |
| `a+b`                       | Matches "a" one or more times followed by "b".  | "ab", "aaab"                       |
| `a?b`                       | Matches "a" zero or one time followed by "b".   | "b", "ab"                         |
| `a{2}`                      | Matches exactly two "a"s.                      | "aa"                              |
| `a{2,4}`                    | Matches between two to four "a"s.             | "aa", "aaa", "aaaa"              |
| `[abc]`                     | Matches any single character within the brackets. | "a", "b", "c"                    |
| `[^abc]`                    | Matches any single character not in the brackets. | "d", "e"                         |
| `(abc|def)`                 | Matches either "abc" or "def".                | "abc", "def"                     |
| `\d`                        | Matches any digit (equivalent to `[0-9]`).     | "0", "1", "2"                     |
| `\D`                        | Matches any non-digit character.                | "a", "!"                          |
| `\w`                        | Matches any word character (alphanumeric plus underscore). | "a", "A", "1", "_"              |
| `\W`                        | Matches any non-word character.                 | " ", "!", "#"                     |
| `\s`                        | Matches any whitespace character (space, tab, newline). | " ", "\t"                       |
| `\S`                        | Matches any non-whitespace character.           | "a", "1", "!"                     |

---

## 2. **Explanation of Regex Syntax and Special Characters**

| Character                 | Description                                   |
|---------------------------|-----------------------------------------------|
| `.`                       | Matches any character except newline.        |
| `^`                       | Asserts the start of a string.              |
| `$`                       | Asserts the end of a string.                |
| `*`                       | Matches zero or more occurrences of the preceding element. |
| `+`                       | Matches one or more occurrences of the preceding element. |
| `?`                       | Matches zero or one occurrence of the preceding element. |
| `{n}`                     | Matches exactly `n` occurrences of the preceding element. |
| `{n,}`                    | Matches `n` or more occurrences of the preceding element. |
| `{n,m}`                   | Matches between `n` and `m` occurrences of the preceding element. |
| `|`                       | Acts as a logical OR between expressions.   |
| `()`                      | Groups patterns and captures matched text.  |
| `[]`                      | Matches any single character within the brackets. |
| `\`                       | Escapes a special character.                 |

---

## 3. **Useful Regex Flags**

| Flag                      | Description                                   |
|---------------------------|-----------------------------------------------|
| `i`                       | Case-insensitive matching.                   |
| `g`                       | Global search (find all matches).           |
| `m`                       | Multiline matching (changes `^` and `$` behavior). |

---

## 4. **Examples of Common Regex Use Cases**

| Use Case                  | Regex Pattern                               | Example                             |
|---------------------------|--------------------------------------------|-------------------------------------|
| **Email Validation**      | `^[\w-\.]+@([\w-]+\.)+[\w-]{2,4}$`        | "example@mail.com"                 |
| **URL Validation**        | `^(https?:\/\/)?([\w\-]+\.)+[\w\-]+(\/[\w\-./?%&=]*)?$` | "http://www.example.com"          |
| **Phone Number Validation**| `^\+?(\d[\d- ]{7,}\d)$`                   | "+1234567890", "123-456-7890"      |
| **Date Validation**       | `^(0[1-9]|1[0-2])\/(0[1-9]|[12][0-9]|3[01])\/(\d{4})$` | "12/31/2024"                       |

---

This **Regex Cheat Sheet** provides a comprehensive overview of common patterns, syntax, and special characters used in regular expressions.


Key Command
Ctrl/Cmd + B Toggle bold
Ctrl/Cmd + I Toggle italic
Alt+S (on Windows) Toggle strikethrough1
Ctrl + Shift + ] Toggle heading (uplevel)
Ctrl + Shift + [ Toggle heading (downlevel)
Ctrl/Cmd + M Toggle math environment
Alt + C Check/Uncheck task list item
Ctrl/Cmd + Shift + V Toggle preview
Ctrl/Cmd + K V Toggle preview to side