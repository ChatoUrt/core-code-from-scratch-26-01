# core-code-from-scratch-26-01

## ---The Hashtag Generator---

* [Test](https://www.codewars.com/kata/52449b062fb80683ec000024/train/javascript)

Solution / /

``` javascript 
function generateHashtag(str) {
    const hash = '#';
    str = str.split(/[ ]+/).join(' ');
    if (str.length < 140){
        if (str.trim() !== ''){
            let arr = str.split(' ');
            for (var i = 0; i < arr.length; i++) arr[i] = arr[i].charAt(0).toUpperCase() + arr[i].slice(1);
            let together = arr.join(' ').replace(/[' ']/g, '');
            return `${hash}${together}`;
        }
    }
        return false
}
```

---
## ---String Incrementer---

* [Test](https://www.codewars.com/kata/54a91a4883a7de5d7800009c/train/javascript)

Solution / /

``` javascript
function incrementString(str) {
  let match = str.match(/\d+$/);
  if (!match) {
    return str + "1";
  }
  let num = match[0];
  let newNum = (parseInt(num) + 1).toString();
  while (newNum.length < num.length) {
    newNum = "0" + newNum;
  }
  return str.replace(/\d+$/, newNum);
}
```
