The bug was that num1 and num2 were read as strings rather than integers.


I would fix it by changing line 9 to 
``` 
let result = Number(num1) + Number(num2)
 ```


1. citylots.json
2. part2.js
3. 11.7 MB
4. 63.52ms
5. Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/88.0.4324.104 Safari/537.36
6. Apache
7. Tue, 26 Jan 2021 22:14:13 GMT
8. application/json
9. fetchData()