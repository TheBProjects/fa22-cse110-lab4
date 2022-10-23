1. It will print 3. This is explainable because of the fact that variable i was declared with the var keyword, and therefore, it can be accessed beyond its scope, the for loop, as long as it's still accessed inside the same function it was declared in
2. It will print 150. This is because the last value of the variable before the loop terminated was 150(calculated by 300, the last value of the array multiplied by 1 - 0.5 or 0.5). Since it's declared with var, it can be accessed outside of its scope as long as it's in the function scope
3. It will print 150. This is the last value of finalPrice, calculated by the last value of discountedPrice before the loop terminated, found earlier on in question 2, multiplied by 100, so 15000. Rounded, so still 15000, then divided by 100 so back to 150. This works because the variable is in the same scope as when it was accessed(and its var)
4. It will return he array [50, 100, 150]. The first value, 50, comes from how the first value of prices is 100 and it was multiplied by 1 - discount = 0.5. Then it was processed into Math.round(discountedPrice * 100) / 100, but since it's a whole number, this did nothing and we still have 50. It was later pushed in. The next element in prices is 200, which was multiplied by 0.5 and since that's also a whole number, it was unaffected by line 8 and got pushed in and we get 100 as our second element. Our last element is 300, multiplied by 0.5 = 150, and since it's a whole number, it's not affected by line 8 and got pushed in. This ends the loop and it gets returned. There was no error since the return is in the same scope as the array and the array was initialized with var. 
5. It got an error. This is because the scope of i is the for loop it was declared in and it was declared with let, not var, meaning that it can't be accessed outside
6. It got an error. This is because the scope of that variable is in the for loop, so it can't be accessed outside
7. It will return 150. This is the correct value of finalPrice, as we saw from 3. This is because it's accessed in the same scope, the general function scope.
8. It will return [50, 100, 150]. This is the correct value, and it got returned because of the fact that it's in the same scope as when it was returned
9. An error will be thrown. Once again, i is declared in the for loop with let. We want to access it outside of its scope, but we can't since it uses let.
10. It will print out 3. This is because of the fact that the variable is in the same scope as the print statement, so even with const, it still gets printed
11. The array [50, 100, 150]. This is because it was returned at the same scope as it was declared, so even with const, it still gets returned
12. A. student.name
B. student['Grad Year']
C. student.greeting()
D. student['Favorite Teacher'].name
E. student.courseLoad[0]
13. A. 32, because of the fact that we're adding a string to an int, so the string causes the addition to become concatenation
B. 1, because there's no - option for string, it turns into subtraction, so it becomes 3 - 2 = 1
C. 3 + null = 3 because null defaults to 0 in integer addition
D. 3null, because in this case, the '3' string makes the + become concatenation, so we get 3null
E. 4, because true resolves to 1 in integer addition and so we get 1 + 3 = 4
F. 0, because false resolves to 0 and null resolves to 0 as well. In integer addition 0 + 0 = 0, which is what we get
G. 3undefined, because the string resolves the + to concatenation
H. NaN. This is because of the fact that - resolves to integer subtraction since strings don't have a - option. Therefore, it resolves to integer subtraction, but 3 - undefined isn't defined, so it's NaN
14. A. true, because 2 > 1 in integer math
B. true, because 2 < 12 in integer math
C. true, because 2 = 2 in integer math
D. false, because 2 is an int while '2' is a string
E. false, because true resolves to 1 and 1 != 2
F. true, because Boolean(2) resolves to true since 2 is a number that isn't 0. Therefore, true == true
15. == resolves the type differences and compares them. For example 2 == '2' is true because '2' gets resolved into an int and it becomes integer equality. === is strict on type differences and requires them to be the exact same type. '2' === 2 is false because they are different times
17. [2,4,6]. We pass in doSomething, which multiplies its parameter by 2 and returns it. The for loop goes through every element in array and pushes doSomething(array[i]) into newArr, which is empty. In effect, this means that every iteration pushes array[i] * 2 into newArr, which means that newArr should be array, but the elements are multiplied by 2. Therefore, [2,4,6]
19. 1\n4\n3\n2. We first run the synchronous actions top down, so we first print 1 and then 4. We now go into the event loop and we print 3 first since the timeout is set to zero so it runs instantly. Then we print 2 one second afterward since the timeout is 1000.
