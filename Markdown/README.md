# Hello World! 
`(# Space behind the hash symbols is required.)`
`#: The biggest headline (Title)`

# Markdown Syntax
## 1. Title (HeadLine)
* It is supported from 1 to 6.
```markdown
# Title 1
## Title 2
### Title 3
#### Title 4
##### Title 5
###### Title 6
```

# Title 1
## Title 2
### Title 3
#### Title 4
##### Title 5
###### Title 6

```
h1
=
h2
-
```

h1
=
h2
-

## 2. Horizontal Line
* If you enter these things(`*` or `-`, `_`) more than three times, you can make horizontal line.
```
***
---
_____
```
***
---
_____

Paragraph 1

***

Paragraph 2 

***

Sentence1
Sentence2

Sentence1 
(input Enter)

Sentence2

Sentence1(input space 2times)  
Sentence2

Sentence1(br tag)<br>
Sentence2

## Decoration
```markdown
**Bold**
__Bold__
** Bold ** <- It does not work.
*italic*
~~strikethrough~~
***Bold italic***
<u>underline</u>
```
**Bold**
__Bold__
** Bold ** <- It does not work.
*italic*
~~strikethrough~~
***Bold italic***
<u>underline</u>

##Quotation 
* Quoting someone else's words and making a feeling of  emphasizing specific text through a box  ``>` and it can be nested.
``` markdown
> First Quotation
>> Second Quotation
>>> Third Quotation
>>>> Fourth Quotation
```
> First Quotation
>> Second Quotation
>>> Third Quotation
>>>> Fourth Quotation

> That Which Does Not Kill Us Making Us Stronger. - *Nietzsche(German philosopher)*

## List
* list -> ordered list, unorderd list
### Ordered list
```
1. First
    1. the first of the first
    2. the second of the first
2. Second
3. Third
```
1. First
    1. the first of the first (When it reaches a certain length, it will automatically line break while maintaining the current tab (indentation) level.)
    2. the second of the first
2. Second
3. Third

```
1. First
1. First
1. First
```
1. First
1. First
1. First

```
1. First
3. First
2. First
```
1. First
3. First
2. First

```
3. First
2. Second
1. Third
```

3. First
2. Second
1. Third
* When using a numbered list: Arrange it in ascending order (1, 2, 3, 4, 5...) based on the first appearing number, without regard to any numbers that appear in between.

### unordered list
```
* list
- list
+ list
    * Indentation is possible.
    * using space key is also possible.
```
* list
- list
+ list
    * Indentation is possible.
    * using space key is also possible.

## Code
    * This is the raw syntax, presented as is without applying markup syntax.

### Single-line code
* \` backslash is covered by backtick.

`print('Hello World')` <br>
This person is `real`.

### Multi-line code (Code block)
```
If you write the language name next to the backtick on the top line as shown below, the color is applied.
```

```python
condition = True

if condition :
    print('OK!')
else:
    print('NOT OK!')
```
```HTML
print('hello');
```

## Table
```
|Title1|Title2|Title3|
|-----|-----|-----|
|line1-1|row1-2|row1-3|
|row2-1|row2-2|row2-3|
```
|Title1|Title2|Title3|
|-----|-----|-----|
|line1-1|row1-2|row1-3|
|row2-1|row2-2|row2-3|

|Title1|Title2|Title3|
|:-|:-:|-:|
|Left Alignment|Center Alignment|Right Alignment|


## Link
### Text Link
```
[The text to be displayed](the link address to be connected)
```
[Naver](https://naver.com)

### Insert Image
```
![Description](the link address to be connected)
```
![Cat](https://cdn.pixabay.com/photo/2014/04/13/20/49/cat-323262_1280.jpg)

### Add a link to the image
[![Cat](https://cdn.pixabay.com/photo/2014/04/13/20/49/cat-323262_1280.jpg)](https://naver.com)

## Checkbox
- [ ] Task 1
- [x] Task 2
```
Markdown Checkboxes is installed.
```