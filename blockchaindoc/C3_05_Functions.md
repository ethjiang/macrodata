Hello and welcome back, in this chapter, we will discuss functions.

大家好，欢迎回来，在本章中，我们将讨论函数。

A function is a reusable piece of code that can be called anywhere in your program, eliminating the need for repetitive code.

函数是一段可重用的代码，可以在程序中的任何地方调用，从而消除了重复代码的需要。

Let me explain to you with an example.

让我举个例子来解释一下。

Let’s get back to the remix,

让我们回到remix，

here let’s declare a uint variable that will be public and name it a mynumber;

这里让我们声明一个uint变量，它将是公共的，并将其命名为mynumber；

now suppose we want to update this number. for that, we need to declare a function.

现在假设我们想更新这个数字。为此，我们需要声明一个函数。

The syntax for declaring a function goes like this, first, you write the function keyword then you declare the name of the function let’s say update number, and then brackets. and after that the curtly brackets.

声明函数的语法如下，首先，您编写函数关键字，然后声明函数的名称，比如更新号，然后加括号。然后是简短的括号。

every function is declared this way in solidity.

每个函数在solidity中都是这样声明的。

Now inside these curly brackets, you write a code according to any logic you want to perform.

现在，在这些花括号内，您可以根据要执行的任何逻辑编写代码。

For now, we want to update this number so let’s assign 10 to the number in the bracket.

现在，我们想更新这个数字，所以让我们给括号中的数字赋值10。

Now in order to call this function we also need to declare the function visibility. We will discuss visibility in detail in the next chapter. for now, just remember to add visibility as public. and compile our smart contract and deploy.

现在，为了调用此函数，我们还需要声明函数可见性。我们将在下一章中详细讨论可见性。现在，只需记住添加公共可见性。并编译我们的智能合约并部署。

now below here, you can see a button for the function. currently, the value is 0 for the mynumber now let’s call the function and check the value again, right the value is 10 now.

现在，在下面，您可以看到该功能的按钮。目前，mynumber的值是0。现在让我们调用函数并再次检查该值，正确的值是10。

Now suppose I want to set a dynamic value to my number, I want to take the value from user input and whatever is input I want to set that for my number.

现在，假设我想为我的数字设置一个动态值，我想从用户输入中获取该值，无论输入的是什么，我都要为我的号码设置该值。

for that function has something called arguments. we can take arguments in the function by passing the variable type and name in the brackets here. so let’s add a uint value in the brackets and in the function set the number to the value.

因为这个函数有一个叫做arguments的东西。我们可以通过在括号中传递变量类型和名称来获取函数中的参数。因此，让我们在括号中添加一个uint值，并在函数中将数字设置为该值。

now deploy this contract again, and now you can see we have one input field in front of the button, right now the value for the Myint is 0, now let’s pass 5 and call this function. and check the value again right now,

现在再次部署这个合约，现在你可以看到我们在按钮前面有一个输入字段，现在Myint的值是0，现在让我们传递5并调用这个函数。现在再次检查该值，

the value is set to 5.

该值被设置为5。

let’s set another value to 8. and call the function,

让我们将另一个值设置为8。并调用该函数，

working perfectly.

工作完美。

you can accept multiple arguments in the function just by adding quama and passing variables just like uint. lloo

只需添加quama并像uint一样传递变量，就可以在函数中接受多个参数。你好

Let’s say we want to build a calculator which returns the addition of 2 numbers.

假设我们想构建一个计算器，返回2个数字的加法。

You might have guessed how to use functions to do that.

你可能已经猜到如何使用函数来做到这一点。

so let’s built the calculator function.

那么，让我们构建计算器函数。

we do this by defining the function keyword and then the function name as a calculator and this will accept 2 arguments of type unsigned integer num-1 and num-2.

我们通过将函数关键字和函数名定义为计算器来实现这一点，这将接受2个无符号整数num-1和num-2类型的参数。

the function is public and then inside the function, we again declare one variable of type unsigned integer, addition, which is equal to num-1 plus num-2.

函数是公共的，然后在函数内部，我们再次声明一个无符号整数类型的变量addition，它等于num-1加num-2。

we have performed the operations but how to show results to the user.

我们已经执行了操作，但如何向用户显示结果。

For that we need to return this result, this can be done using the return keyword and then return the variable addition here.

为此，我们需要返回此结果，这可以使用return关键字完成，然后在此处返回变量addition。

in solidity, we also need to specify what we are returning in front of the function at the end. the returning type is uint.

在solidity中，我们还需要指定在函数末尾返回什么。返回类型为uint。

we also need to add pure here. that we will discuss later.

我们还需要在这里添加纯。我们稍后会讨论。

now let’s compile and deploy this contract and you can see we are getting input field like last time let’s pass 2 quama 3 and call the function now you can see we are getting 5 which is the result.

现在让我们编译和部署这个合约，你可以看到我们得到了输入字段，就像上次一样，让我们传递2 quama 3并调用函数，现在你可以看到，我们得到了5，这是结果。

At the beginning of this chapter, I said reusable code. Now let me explain to you what I meant by that.

在本章的开头，我提到了可重用代码。现在让我解释一下我的意思。

Suppose we also want to perform multiplication and return the result, i know what you are thinking just add one more variable multiplication do the multiplication, and return along with addition.

假设我们还想执行乘法并返回结果，我知道你在想什么——只需再加一个变量乘法，再进行乘法，并与加法一起返回。

and you are correct also. but suppose we also want to get only multiplication and not addition then what? declare one more function and return multiplication?

你也是对的。但是，假设我们也只想得到乘法而不想得到加法，那么呢？再声明一个函数并返回乘法？

let’s see.

让我们看看。

build a function above here named multiply this will accept two arguments uint num-1 and uint num-2. and this will be public pure and returns uint

在这里构建一个名为multiply的函数，它将接受两个参数uintnum-1和uintnum-2。这将是公共纯的，返回uint

inside it we will return num-1 into num-2. that’s it.

在里面，我们将把num-1返回到num-2。就是这样。

now below here the addition line let’s declare one more uint multiplication and now call the above function here and pass the num1 and num2 values.

现在，在下面的加法行中，让我们再声明一个uint乘法，现在在这里调用上面的函数并传递num1和num2值。

note that you do not need to use the same argument values as I did.

请注意，您不需要使用与我相同的参数值。

you can use num3 and num4 as well in the multiply function just make sure that you are returning the result also with num3 into num4.

您也可以在乘法函数中使用num3和num4，只需确保您将结果与num3一起返回到num4中即可。

now let’s add one more return multiplication and also update in the returns.

现在，让我们再添加一个返回乘法，并更新返回值。

That's it. Now let's deploy the contract. Now you can perform addition and multiplication in the same function, and also get only multiplication.

就是这样。现在让我们部署合同。现在你可以在同一个函数中执行加法和乘法，也可以只得到乘法。

This reusing function is very helpful when there are much larger functions.

当有更大的函数时，这种重用函数非常有用。

So that was all about the functions, now in the next chapter complete an assignment.

以上就是关于函数的内容，现在在下一章中完成一项作业。

see you in the next chapter.

下一章见。