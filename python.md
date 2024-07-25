# Python Interview Questions & Answers

#### 1. Write a program to list the function?

#### 2.to list even and odd numbers
#### 3.to print functions
#### 4.dict fun
#### 5. Difference between compiler and interpreter?

#### 6. 𝗘𝘅𝗽𝗹𝗮𝗶𝗻 𝘁𝗵𝗲 𝗱𝗶𝗳𝗳𝗲𝗿𝗲𝗻𝗰𝗲 𝗯𝗲𝘁𝘄𝗲𝗲𝗻 𝗹𝗶𝘀𝘁𝘀 𝗮𝗻𝗱 𝘁𝘂𝗽𝗹𝗲𝘀 𝗶𝗻 𝗣𝘆𝘁𝗵𝗼𝗻.
Lists are mutable, meaning their elements can be changed but Tuples are immutable.

#### 7. 𝗪𝗵𝗮𝘁 𝗶𝘀 𝗮 𝗗𝗮𝘁𝗮𝗙𝗿𝗮𝗺𝗲 𝗶𝗻 𝗽𝗮𝗻𝗱𝗮𝘀?
A DataFrame is a 2-dimensional labelled data structure, similar to a spreadsheet.

#### 8. 𝗥𝗲𝘃𝗲𝗿𝘀𝗶𝗻𝗴 𝘁𝗵𝗲 𝘄𝗼𝗿𝗱𝘀 𝗶𝗻 𝗮 𝘀𝘁𝗿𝗶𝗻𝗴 𝗶𝗻 𝗣𝘆𝘁𝗵𝗼𝗻
def reverse_words(s: str) -> str:
 words = s.split()
 reversed_words = reversed(words)
 return ' '.join(reversed_words)

#### 9. 𝗪𝗿𝗶𝘁𝗲 𝗮 𝗣𝘆𝘁𝗵𝗼𝗻 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝘁𝗼 𝗰𝗼𝘂𝗻𝘁 𝘁𝗵𝗲 𝗻𝘂𝗺𝗯𝗲𝗿 𝗼𝗳 𝘃𝗼𝘄𝗲𝗹𝘀 𝗶𝗻 𝗮 𝗴𝗶𝘃𝗲𝗻 𝘀𝘁𝗿𝗶𝗻𝗴?
def count_vowels(string: str) -> int:
 vowels = "aeiouAEIOU"
 vowel_count = 0
 for char in string:
 if char in vowels:
 vowel_count += 1
 return vowel_count
