# Poetry Club Door Policy
## My solution

```javascript
export function frontDoorResponse(line) {
  return line[0];
}

export function frontDoorPassword(word) {
  const FIRST_LETTER = word[0].toUpperCase();
  const REST_OF_WORD = word.slice(1).toLowerCase();

  return FIRST_LETTER + REST_OF_WORD;
}

export function backDoorResponse(line) {
  const LINE_WITHOUT_BLANKS = line.trim();
  const LAST_LETTER = LINE_WITHOUT_BLANKS[LINE_WITHOUT_BLANKS.length - 1];

  return LAST_LETTER;
}

export function backDoorPassword(word) {
  return `${frontDoorPassword(word)}, please`;
}
```
