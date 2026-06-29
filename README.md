## Regex Cheat Sheet

```text
.       Any character
*       0 or more
+       1 or more
?       0 or 1
^       Start of line
$       End of line
|       OR
()      Group
[]      Character set
[^]     Negated character set
```

### Character Classes

```regex
[abc]       a or b or c
[a-z]       lowercase letter
[A-Z]       uppercase letter
[0-9]       digit
[a-zA-Z]    any letter
[a-zA-Z0-9] alphanumeric
[^0-9]      not a digit
```

### Shortcuts

```regex
\d      digit (0-9)
\D      not digit

\w      word character
\W      not word character

\s      whitespace
\S      not whitespace
```

### Quantifiers

```regex
a*          0 or more a
a+          1 or more a
a?          0 or 1 a

a{3}        exactly 3 a
a{2,5}      2 to 5 a
a{3,}       3 or more a
```

### Common Patterns

#### IP Address

```regex
\d+\.\d+\.\d+\.\d+
```

#### Email

```regex
[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}
```

#### URL

```regex
https?://\S+
```

#### Numbers Only

```regex
^\d+$
```

#### Letters Only

```regex
^[A-Za-z]+$
```

#### Starts With

```regex
^ERROR
```

#### Ends With

```regex
OK$
```

#### Contains Both Words

```regex
apple.*banana|banana.*apple
```

#### Find Serial Number

```regex
Serial Number
```

### grep Examples

```bash
grep "ERROR" log.txt

grep -i "error" log.txt

grep -E "cat|dog" file.txt

grep -E "[0-9]+" file.txt

grep "^root" /etc/passwd

grep "bash$" /etc/passwd

grep -r "password" .

grep -n "ERROR" log.txt

grep -v "INFO" log.txt
```

### Most Useful 10 Patterns

```regex
^text          Start with text
text$          End with text
^text$         Exact match
\d+            One or more digits
\w+            One or more word chars
\s+            One or more spaces
[a-z]+         Lowercase word
[A-Z]+         Uppercase word
(cat|dog)      cat OR dog
.*             Anything
```

For log analysis and grep work, the patterns are:

```regex
^  $  .  *  +  ?  []  ()  |  \d  \w  \s
```
