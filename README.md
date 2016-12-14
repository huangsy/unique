# unique
数组去重

### 文艺解法

```javascript
function unique(arr) {
  return Array.from(new Set(arr));  
}
```

### 二逼解法

```javascript
function unique(arr) {
  var hash = {};
  var result = [];
  for (var i = 0, len = arr.length; i < len; i++) {
    var item = arr[i];
    var key = typeof item + JSON.stringify(item);
    if (!hash[key]) {
      hash[key] = true;
      result.push(item);
    }
  }
  return result;
}
```
