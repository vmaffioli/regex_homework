# REGEX
<a href="https://docs.microsoft.com/en-us/dotnet/standard/base-types/regular-expression-language-quick-reference">Quick Reference - Microsoft</a>

REGEX - examples &amp;&amp; study material

Expressions need to be surrounded by forward slash - Eg.
/expression/

Always matches the closes word / letter to left without check the whole text

Global matching (with g)
Find all matches in the text, no matter whre they are

Engine starts parsing data from left to right, sometimes backtranking when match is not found

Matches are all case sensitive by default

Range examples
[A-Z]  matches any uppercase character from A to Z 
[a-z] matches any lowercase character from A to Z 
[0-9] matches any digit character from 0 to 9
[A-Za-z0-9] we can also combine them


Repetition Metacharacters
Quantifier	Description
*	Matches the previous element zero or more times.
+	Matches the previous element one or more times.
?	Matches the previous element zero or one time.
{n}	Matches the previous element exactly n times.
{n,}	Matches the previous element at least n times.
{n,m}	Matches the previous element at least n times, but no more than m times.


Examples
/cars*/ - matches car, cars and carsssssssssss and many more 

/\d\d\d*/ - matches two digits or more (remember this is starts from zero to more)

/cars+/ - does not match car since it needs to be more more than 1 character ,E.G, cars or carsssssssssss

/\d\d\d+/ - matches three digits or more (remember this is starts from 1 to more)

/car?/ - the  (r) its optional meaning it matches car and cars not carssssssss

/\d{1}/  - matches 1 single digits

/\d{1,}/ - matches 1 or more digits

/\d{1,2}/ - matches 1 to 2 digits


-------------------------------------------------------------------------------

Greedy Expression vs Lazy
Greedy \w+\d+\w+ it maches file1_export from file1_export.sql  since it tries to math as much as possible

Lazy \w+\d+\w+? , this matches file1_ from file1_export.sql  why is gives up when it find the first word character at the end. (Notice we have a question mark at the end of the w "?" )

You can use the lazy format in these quantifiers  *, +. {} ?, you would have something likes this *?, +?, {}?, ??


to remember
- Standart - /expression/
- Case-insensitive - /expression/i
- Dot-matches-all - /expression/s
- Multiline - /expression/m
- Global - /expression/g
- Match anything - .
- Escape = \
- New line = \n
- Tab- \t
- Optional - ?
- Range - []
- Whiste space - \s 
- Negation - ^
- Limit repetition - {}
