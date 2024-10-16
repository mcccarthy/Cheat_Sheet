Here's a cheat sheet for Regular Expressions (Regex) covering syntax, pattern matching, and common use cases in JavaScript and Python in Markdown format.

````markdown
# Regular Expressions (Regex) Cheat Sheet

## Basic Syntax

- **Literal Characters**: Match the exact character.

  - Example: `abc` matches "abc".

- **Meta-characters**:

  - `.`: Matches any character except a newline.
  - `^`: Matches the start of a string.
  - `$`: Matches the end of a string.
  - `*`: Matches 0 or more of the preceding element.
  - `+`: Matches 1 or more of the preceding element.
  - `?`: Matches 0 or 1 of the preceding element.
  - `{n}`: Matches exactly n occurrences of the preceding element.
  - `{n,}`: Matches n or more occurrences.
  - `{n,m}`: Matches between n and m occurrences.

- **Character Classes**:

  - `[abc]`: Matches any one of the characters a, b, or c.
  - `[^abc]`: Matches any character not in the set.
  - `[a-z]`: Matches any lowercase letter.
  - `[A-Z]`: Matches any uppercase letter.
  - `[0-9]`: Matches any digit.

- **Predefined Character Classes**:

  - `\d`: Matches any digit (equivalent to `[0-9]`).
  - `\D`: Matches any non-digit.
  - `\w`: Matches any word character (equivalent to `[a-zA-Z0-9_]`).
  - `\W`: Matches any non-word character.
  - `\s`: Matches any whitespace character (space, tab, newline).
  - `\S`: Matches any non-whitespace character.

- **Grouping and Alternation**:
  - `(abc)`: Groups the pattern "abc".
  - `a|b`: Matches either "a" or "b".

## Flags (Modifiers)

- `g`: Global search (find all matches).
- `i`: Case-insensitive search.
- `m`: Multi-line search (affects `^` and `$`).

## Common Use Cases

### JavaScript

- **Testing a Pattern**:
  ```javascript
  const regex = /abc/;
  console.log(regex.test('abcdef')); // true
  ```
````

- **Matching a Pattern**:

  ```javascript
  const str = 'Hello 123';
  const regex = /\d+/;
  const match = str.match(regex);
  console.log(match[0]); // '123'
  ```

- **Replacing Patterns**:

  ```javascript
  const str = 'I like cats and dogs';
  const newStr = str.replace(/cats|dogs/g, 'animals');
  console.log(newStr); // 'I like animals and animals'
  ```

### Python

- **Importing the `re` Module**:

  ```python
  import re
  ```

- **Searching for a Pattern**:

  ```python
  pattern = r'\d+'
  match = re.search(pattern, 'Hello 123')
  print(match.group())  # '123'
  ```

- **Finding All Matches**:

  ```python
  matches = re.findall(r'\d+', 'I have 2 cats and 3 dogs')
  print(matches)  # ['2', '3']
  ```

- **Replacing Patterns**:

  ```python
  text = 'I like cats and dogs'
  new_text = re.sub(r'cats|dogs', 'animals', text)
  print(new_text)  # 'I like animals and animals'
  ```

## Examples

- **Email Validation**:

  ```regex
  ^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
  ```

- **URL Validation**:

  ```regex
  ^https?:\/\/[^\s$.?#].[^\s]*$
  ```

- **Phone Number Validation** (US Format):

  ```regex
  ^\(\d{3}\) \d{3}-\d{4}$
  ```

- **Extracting Dates (YYYY-MM-DD)**:

  ```regex
  \b\d{4}-\d{2}-\d{2}\b
  ```

## Resources

- [Regex101](https://regex101.com/): Interactive regex testing and debugging.
- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions): JavaScript regex documentation.
- [Python `re` Module Documentation](https://docs.python.org/3/library/re.html): Official Python regex documentation.

---

This cheat sheet provides a quick reference for regex syntax, common methods in JavaScript and Python, and practical use cases.
