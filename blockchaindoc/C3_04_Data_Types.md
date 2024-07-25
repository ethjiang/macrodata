## Data Types
Hello and welcome back, I hope you have completed the exercise successfully and you now understand the structure of a smart contract. In this chapter we will discuss the various data types that are available in the solidity.

## Overview
Every computer program is ultimately, operations on data. Movies you watch, messages you do, apps you use, games you play is all operations on data at gigantic scales managed and directed via programs/codes, Hence data is building block of programming, and ultimately any digital system.

In every programming language, you use variables to store particular data or values. Variables are something that doesn't have a fixed value and can be changed. When you create a variable you reserve some space in the memory of your code.

As you know data is always in the form of Numbers, Letters, and Symbols. These variables follow the rules of what type of data they can store. In programming languages you have to mention which type of data you are storing in your variables, it is called data types.

Every programming language stores the following types of data in variables:

- Boolean - It has two values only that is 0, and 1. It can also be interpreted as True and False, where True implies 1 and False implies 0.
- Integer - It can take any integer value. ex. 1, 4, -10, 23 etc.
- Float - It can take any real value. eg. 0.2, 32, 100.44 etc.
- String - It is simply a combination of any word, letter, symbol, and number. eg 'hello World @ 123', '0xlight' etc.

## Data types in Solidity
Now coming back to solidity we have Integers, String, Boolean, and Address. There are two new things here compared to other programming languages.

- A new data type called Address, You won't find it in other programming languages.
- Solidity doesn't have a float data type means it doesn't deal with fractional numbers.

Let's look at each data type carefully in detail,

First the simplest one,

## Boolean
It can store only two values, which are True, and False. Keyword bool is used to create a boolean variable

```
bool public a = true;
bool public b = false;
```
This is how you write a bool data type variable and assign value.

## Integers

Integers are a data type used to represent whole numbers. Solidity supports several integer types with different ranges and characteristics. Here are the commonly used integer types in Solidity:

**int:** Signed integer type. It can store both positive and negative whole numbers. For example, int8, int16, int32, int64, etc., represent signed integers with different bit sizes (8, 16, 32, 64 bits, etc.).

**uint:** Unsigned integer type. It can only store non-negative whole numbers. Like int, it also comes in various sizes such as uint8, uint16, uint32, uint64, etc.

The size of an integer type in Solidity is determined by the number of bits it occupies. For instance, int8 occupies 8 bits, int16 occupies 16 bits, and so on. Similarly, uint8 occupies 8 bits, uint16 occupies 16 bits, and so forth.

The bounds of integers and unsigned integers (uints) in Solidity can be determined by their bit sizes

he bounds of integers and unsigned integers (uints) in Solidity can be determined by their bit sizes. The bounds represent the range of values that can be stored within a particular integer type. The general formula to calculate the bounds is as follows:

For signed integers (int):

- The lower bound is −2^(n−1), where n is the number of bits.
- The upper bound is 2^(n−1)−1.

For unsigned integers (uint):

- The lower bound is 0.
- The upper bound is 2^n−1, where n is the number of bits.

Let's take a couple of examples:

int8: Signed integer with 8 bits.

- Lower bound: -128
- Upper bound: 127

uint16: Unsigned integer with 16 bits.

- Lower bound: 0
- Upper bound: 65535

## Strings
String type is used for data values that are made up of ordered sequences of characters, such as "hello world" or “Dappworld123”.

You can put any character in Double quotes(” “) or Single quotes(‘ ‘) and it is a string, simple as that.

```
// -------- Correct Syntax --------
string a = "Hello World"

string a = 'Hello World'

//  -------- Incorrect -------
string a = " Hellow World '
```

## Bytes
In Solidity, the bytes type is a dynamically sized byte array. It provides more flexibility as it can hold any binary data. You can access individual bytes within a bytes variable. For example, you can declare a bytes variable as follows: `bytes public data = hex"001122";`

On the other hand, the string type in Solidity is a dynamically-sized UTF-8 encoded string. It is suitable for handling human-readable text. However, Solidity does not allow direct access to individual characters within a string. For example, you can declare a string variable like this: `string public text = "Hello, World!";`

In summary, if you are dealing with raw binary data, it is recommended to use the bytes type. If you are working with human-readable text, then the string type is more appropriate. It is crucial to choose the type that best fits your data and use case.

## Address
This is a new data type introduced in solidity, it is simply an address value that is specifically designed to hold up to 20 bytes, which is the size of an Ethereum address.

Every interaction that happens with the contract is initiated by an address whether its user address or contract address, thus addresses play a crucial role in smart contracts.

The addresses have two types, which are mostly identical:

- address: Holds a 20-byte value (size of an Ethereum address).
- address payable: Same as an address, but with additional features such as transfer and send. These functions let you send Ethereum in the smart contract (we will learn about them in the future)

That is all for this chapter, now in the next chapter complete an assignment, and then we will discuss functions in solidity. See you in the next chapter!