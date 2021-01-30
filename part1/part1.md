1. Since i is declared with "var" it is function scoped so it is in scope by line 11. line 11 will print the value of i, which is the length of prices.

2. Line 12 will print the value of discountedPrice. discountedPrice is redefined every time the loops is run so the value of discountedPrice will be prices[i] * (1-discount) where prices[i] is the last element of prices.

3. Line 13 will print the finalPrice which is discountedPrice after it has been rounded to an even dollar amount in line 7. finalPrice is redefined every iteration of the loop so the console will log the finalPrice of the last element of prices.

4. The function will return **[ 50, 100, 150 ]**. Each element of the original prices array [100,200,300] was multiplied by 0.5, rounded to the 100th decimal, then pushed to the returned discount array.

5. Line 11 will return a "ReferenceError: i is not defined" Error since i was declared with "let" and therefore only has block scope and is thus undefined outside of the for loop.

6. Line 12 will return "ReferenceError: discountedPrice is not defined" for the same reason in part 5.

7. Although finalPrice is declared with "let" instead of "var" it was declared in the same block as line 13 andd therfore will behave the same way it did in question 3.

8. The function will return **[ 50, 100, 150 ]**. Each element of the original prices array [100,200,300] was multiplied by 0.5, rounded to the 100th decimal, then pushed to the returned discount array. Since discounted and finalPrice are declared at the beginning of the function, they are not affected by being declared by "let" instead of "var." discountedPrice is  reinitialized every iteration of the loop anyway so it is not affected by being declared with "let" instead of "var"

9. Since const has the same scope as let, line 11 will error the same way it does in question 5.

10. Since const has the same scope as let, line 12 will error the same way it does in question 6.

11. since finalPrice is initialized with const, it cannot change from its initial value. So the console will print 0.

12. The fuction will error with the bottom error since line 7 attempts to change the value of the constant variable finalPrice.
    ```
    finalPrice = Math.round(discountedPrice*100)/100;
                   ^

    TypeError: Assignment to constant variable.
    ```

13. A. student.name
    
    B. student["Grad Year"]

    C. student.greeting()

    D. student["Favorite Teacher"].name

    E. student.courseLoad[0]

14. A. ***'32'***, since this is string concatentation(any string + something is string concat), 2 is converted to a string and concatenated to the end of '3'
    
    B. ***1***, since the - sign is Arithmetic when applied to a string, '2' is converted to an int.

    C. ***3***, since in Arithmetic, null is converted to 0

    D. ***'3null'***, since in concatenation null is ocnverted to the string 'null'

    E. ***4***, since in Arithmetic, true is converted to 1

    F. ***0***, since in Arithmetic both null and false are 0

    G. ***'3undefined'***, since in concatenation undefined is converted to the 
    string 'undefined'
    H. ***NaN***, since in arithmetic the conversion of undefined to an int is NaN and 3 - NaN is NaN

15. A. ***true***, since in conversion everything is converted to numbers, '2' -> 2 and 2 is greater than 1
    
    B. ***false***, since in conversion everything is converted to numbers, '2' -> 2, '12' -> 12 amn 2 is not greater than 12

    C. ***true***, since in conversion everything is converted to numbers, '2' -> 2 and 2 is the same as 2

    D. ***false***, 2 and '2' are different types

    E. ***false***, since in conversion everything is converted to numbers, true -> 1 and 1 is not the same as 2

    F. ***true***, Boolean(2) gets converted to true which is the same type and same value as true

16. the === operator returns all comparisons of variables of different types as false, while == attempts to convert to numbers first

17. ***How are you*** gets printed. true gets converted to 1 in 2 == 1 so that returns false. Then 2 gets converted to true when evaluated as boolean. so the second got block gets executed.

18. ```
    for( var property in statistics) {
        if(property[0] == 'r' || statistics[property] % 2) {
            console.log(statistics[property]);
        }
    }
    ```

19. It will return ***[ 6, 8, 10 ]***, For each value in the array [1,2,3] the value of each element will be passed to doSomething and pused to the returned array. Each call of doSomething addes 2 to the parameter num before multiplying it by 2. This results in each value in the array being added to 2 then multiplied by 2.

20. ```
    var intervalID = setInterval(printTime, 1000);

    function printTime() {
        let d = new Date();
        let time = d.toLocaleTimeString();
        console.log(time);
    }
    ```

21. ```
    1
    4
    3
    2
    ```

    There will be a 1 second delay before 2 is logged to console. 3 will not be logged until the next event cycle.



