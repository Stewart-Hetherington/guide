---
title: Specify Only the Lower Number of Matches
---
## Specify Only the Lower Number of Matches

Remember `/ha{3,}h/` will only return `true` if the letter `a` appears three times between two letter h's. Unlike the previous lesson where we learned to specify between two numbers ( a minimum and a maximum ) - `/a{2,4}/` - when using a single number ( minimum number ) between the curly brackets, the regular expression will only return `true` where the expression is at least that length. 

```
let A4 = "haaaah";
let A2 = "haah";
let A100 = "h" + "a".repeat(100) + "h";
let multipleA = /ha{3,}h/;
multipleA.test(A4); // Returns true ( a > 3 )
multipleA.test(A2); // Returns false ( a < 3 )
multipleA.test(A100); // Returns true ( a > 3 )
```

## Spolier Alert!


## Solutuion: 

```
let haStr = "Hazzzzah";
let haRegex = /haz{4,}ah/i;
let result = haRegex.test(haStr);
```
