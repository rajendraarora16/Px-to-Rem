# Px-to-Rem

A simple JS function to convert `px` to `rem` while writing CSS:

```
const pxToRem = (px: any, base = 16) => {
    let tempPx = px;
    if (typeof px === "string" || px instanceof String)
        tempPx = tempPx.replace("px", "");

    tempPx = parseInt(tempPx);
    return (1 / base) * tempPx + "rem";
};

export default pxToRem;
```
