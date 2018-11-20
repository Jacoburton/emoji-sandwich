## 🥪
# emoji-sandwich

*Parse a string for emojis and wrap them in your chosen tag.*

Useful when handling user generated data and want to emphasize emojis and make them larger.

Example
```
import emojiSandwich from 'emoji-sandwich';

emojiSandwich.wrap("this 🥪😍", "<span class='emoji'>", "</span>")
```

Results in

```
this <span class='emoji'>🥪</span><span class='emoji'>😍</span>
 ```

Using regex replace or itterating through string indexes doesn't work as expected when emojis are present due to some using two code units. This is a lightweight package that uses Runes to split the string and a regex to test if the character is an emoji.