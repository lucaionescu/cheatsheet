```javascript
// Print colors in the console
printColors = (colors) => {
    console.log(
            '%c     '.repeat(colors.length),
            ...colors.map(x => ('background:' + x))
            );
};
```
