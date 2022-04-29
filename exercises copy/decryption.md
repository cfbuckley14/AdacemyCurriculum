# Decryption Tech Test

**Language/Framework**: Any language, frameworks allowed but not necessary  
**Length**: Spend no more than 4 hours on this  
**Submission**: Host on iO dev server

For this technical test you will build a page that takes a list of numbers in a single input and decrypts them into a message output.

- The algorithm used to encrypt messages is a substitution cypher, a normal substitution cypher would be:
  - `a = 1`, `b = 2` up to `z = 26`
- The cypher for our encryption is shifted by 7:
  - `a = 8`, `b = 9` up to `z = 33`
- Numbers above `33` still represent letters, when divided by `27` so `216` is a valid number (`8*27 = 216 = a`)
- Numbers may need to be divided by 27 multiple times. 5,832 is a valid number (`8*27*27 = 5,832 = a`)
- Numbers not divisible by 27 are invalid
- Numbers below `8` should be treated as space characters
- Numbers that are less than `8` when divided by `27` are also space characters (`6*27 = 162 = <a space character>`)
- The first letter of the message should be output as capital, all others as lowercase

- An example of an encrypted message could be:
  - `15 16 6 27 12 8 20` which is `Hi team`
- The same message could also be:
  - `405 432 4374 27 12 157464 540`

- We don't want to give away the secret algorithm, so the decryption should be done on the back-end
- Please focus on clean, tested code
- You can do this as an API back-end with AJAX, or a normal form submission
