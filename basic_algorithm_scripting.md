# 1.Reverse a String
```
function reverseString(str) {
  // 请把你的代码写在这里
  return str.split("").reverse().join("");
}

reverseString("hello");
```

# 2.Factorialize a Number
```
function factorialize(num) {
  // 请把你的代码写在这里
  return (num<=0)?1:num*factorialize(num-1);
}

factorialize(5);
```

# 3.Check for Palindromes
```
function palindrome(str) {
  // 请把你的代码写在这里
  if(str.length==1){
    return true;
  }
  
  str=str.toLowerCase().replace(/[^0-9a-z]/g,"");
  return (str.split("").reverse().join("")==str)?true:false;
}



palindrome("eye");

```

# 4.Find the Longest Word in a String
```
function findLongestWord(str) {
  // 请把你的代码写在这里
  var Array=str.split(" ");
  var longest=0;
  for(var i=0;i<Array.length;i++){
    if(Array[i].length>longest){
      longest=Array[i].length;
    }
  }
  return longest;
}

findLongestWord("The quick brown fox jumped over the lazy dog");
```

# 5.Title Case a Sentence
```
function titleCase(str) {
  // 请把你的代码写在这里
  str=str.toLowerCase().split(" ");
  for(var i=0;i<str.length;i++){
    str[i]=str[i].substring(0,1).toUpperCase()+str[i].substring(1);
  }
  return str.join(" ");
}

titleCase("I'm a little tea pot");
```

# 6.Return Largest Numbers in Arrays
```
function largestOfFour(arr) {
  // 请把你的代码写在这里
  var newArray=[];
  for(var i=0;i<arr.length;i++){
    arr[i].sort(function(a,b){return b-a;});
    newArray.push(arr[i][0]);
  }
  return newArray;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```

# 7.Confirm the Ending
```
function confirmEnding(str, target) {
  // 请把你的代码写在这里
  return (str.lastIndexOf(target)+target.length==str.length)?true:false;
}

confirmEnding("Bastian", "n");
```

# 8.Repeat a string repeat a string
```
function repeat(str, num) {
  // 请把你的代码写在这里
  var newArray="";
  while(num>0){
    newArray+=str;
    num--;
  }
  return newArray;
}

repeat("abc", 3);
```

# 9.Truncate a string
```
function truncate(str, num) {
  // 请把你的代码写在这里
  if(str.length>num){
    if(num>=3){
      str=str.slice(0,num-3)+"...";
    }else{
      str=str.slice(0,num)+"...";
    }
  }
  return str;
}

truncate("A-tisket a-tasket A green and yellow basket", 11);
```

# 10.Chunk Monkey
```
function chunk(arr, size) {
  // 请把你的代码写在这里
  var newArray=[];
  for(var i=0;i<arr.length;i=i+size){
    newArray.push(arr.slice(i,i+size));
  }
  return newArray;
}

chunk(["a", "b", "c", "d"], 2);
```

# 11.Slasher Flick
```
function slasher(arr, howMany) {
  // 请把你的代码写在这里
  if(arr.length>howMany){
    arr.splice(0,howMany);
    return arr;
  }
  arr=[];
  return arr;
}

slasher([1, 2, 3], 2);
```

# 12.Mutations
```
function mutation(arr) {
  // 请把你的代码写在这里
  arr1=arr[0].toLowerCase();
  arr2=arr[1].toLowerCase().split("");
  for(var i=0;i<arr2.length;i++){
    if(arr1.indexOf(arr2[i])<0){
      return false;
    }
  }
  return true;
}

mutation(["hello", "hey"]);
```

# 13.Falsy Bouncer
```
function bouncer(arr) {
  // 请把你的代码写在这里
  return arr.filter(function(item){
    return Boolean(item);
  });
}

bouncer([7, "ate", "", false, 9]);
```

# *14.Seek and Destroy
```
function destroyer(arr) {
  // 请把你的代码写在这里
  var args=[];
  for(var i=0;i<arguments.length;i++){
    args.push(arguments[i]);
  }
  
  function filtered(item){
    return args.indexOf(item)<0;
  }
  var newArray=arr.filter(filtered);
  return newArray;
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3);
```

# 15.Where do I belong
```
function where(arr, num) {
  // 请把你的代码写在这里
  arr.push(num);
  arr.sort(function(a,b){return a-b;});
  return arr.indexOf(num);
}

where([40, 60], 50);
```

# *16.Caesars Cipher
```
function rot13(str) { // LBH QVQ VG!
  // 请把你的代码写在这里
  var newArray=[];
  for(var i=0;i<str.length;i++){
    if(str.charCodeAt(i)>90||str.charCodeAt(i)<65){
      newArray.push(str.charAt(i));
    }else if(str.charCodeAt(i)>77){
      newArray.push(String.fromCharCode(str.charCodeAt(i)-13));
    }else{
      newArray.push(String.fromCharCode(str.charCodeAt(i)+13));
    }
  }
  
  return newArray.join("");
}

rot13("SERR PBQR PNZC");  // 你可以修改这一行来测试你的代码
```
