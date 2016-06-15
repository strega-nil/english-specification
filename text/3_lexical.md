Lexical Elements
===
[lexical.basic]

A rust input source file shall be in a format which can support all of "Unicode
8.0.0".

> note: somehow reword this

Identifiers
---
[lexical.basic.identifiers]

The following definitions shall be used:

```
letter:
  'a' | 'b' | 'c' | 'd' | 'e' | 'f' | 'g' | 'h' | 'i' | 'j' | 'k' | 'l' | 'm'
  'n' | 'o' | 'p' | 'q' | 'r' | 's' | 't' | 'u' | 'v' | 'w' | 'x' | 'y' | 'z'
  'A' | 'B' | 'C' | 'D' | 'E' | 'F' | 'G' | 'H' | 'I' | 'J' | 'K' | 'L' | 'M'
  'N' | 'O' | 'P' | 'Q' | 'R' | 'S' | 'T' | 'U' | 'V' | 'W' | 'X' | 'Y' | 'Z'
nondigit:
  letter | '_'
digit:
  '0' | '1' | '2' | '3' | '4' | '5' | '6' | '7' | '8' | '9'
```

An identifier is a token, [lexical.basic.keywords], which starts with a letter,
and is followed by any number of identifier continuing characters; or starts
with an '_' and is followed by at least one identifier continuing character. An
identifier continuing character is either a digit or a nondigit. If a token
could be characterized as an identifier, or a keyword, it shall be characterized
as a keyword.

```
identifier:
  letter (digit | nondigit)*
  nondigit (digit | nondigit)+
```

Keywords
---
[lexical.basic.keywords]

A keyword is an identifier which matches the following rule:

```
keyword:
  'abstract' | 'alignof'  | 'as'       | 'become'   | 'box'      | 'break'    | 
  'const'    | 'continue' | 'crate'    | 'do'       | 'else'     | 'enum'     | 
  'extern'   | 'false'    | 'final'    | 'fn'       | 'for'      | 'if'       | 
  'impl'     | 'in'       | 'let'      | 'loop'     | 'macro'    | 'match'    | 
  'mod'      | 'move'     | 'mut'      | 'offsetof' | 'override' | 'priv'     | 
  'proc'     | 'pub'      | 'pure'     | 'ref'      | 'return'   | 'Self'     | 
  'self'     | 'sizeof'   | 'static'   | 'struct'   | 'super'    | 'trait'    | 
  'true'     | 'type'     | 'typeof'   | 'unsafe'   | 'unsized'  | 'use'      | 
  'virtual'  | 'where'    | 'while'    | 'yield'
```
