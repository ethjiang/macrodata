Hello and welcome back. In this chapter, we are going to learn about smart contract structure, so let's open the Remix IDE and get started.

你好，欢迎回来。在本章中，我们将学习智能合约结构，所以让我们打开Remix IDE并开始吧。

Smart contracts have three components. Let's learn about each one of them.

智能合约有三个组成部分。让我们了解一下它们中的每一个。

We have a basic contract here.

我们这里有一份基本合同。

First is the license identifier where you have to mention the license for your code. You may ask why we have to include licenses. We don't usually see this in non-blockchain programming. It's because every smart contract is deployed on the blockchain, which is open to all and is very transparent in nature.

首先是许可证标识符，您必须在其中提及代码的许可证。你可能会问为什么我们必须包括许可证。我们通常在非区块链编程中看不到这一点。这是因为每个智能合约都部署在区块链上，区块链对所有人开放，本质上非常透明。

However, every smart contract can have different licenses, and it depends on the creator or deployer what kind of license they want to apply to their smart contract.

然而，每个智能合约都可以有不同的许可证，这取决于创建者或部署者想要将哪种许可证应用于他们的智能合约。

Now, talking about the syntax, this is how you have to write the license of a smart contract.

现在，谈论语法，这就是你必须如何编写智能合约的许可证。

SPDX License Identifier: MIT.

SPDX许可证标识符：MIT。

Here you have to write SPDX License Identifier as it is, and whatever the license type goes after it, like MIT, GPL, etc.

在这里，您必须按原样编写SPDX许可证标识符，以及其后的任何许可证类型，如MIT、GPL等。

First, while writing contract, you can skip this line and it won't give you an error, but it will show a warning. Apart from that, your code will successfully compile and can be deployed on the blockchain.

首先，在写合同时，你可以跳过这一行，它不会给你一个错误，但会显示一个警告。除此之外，您的代码将成功编译并可以部署在区块链上。

Let’s remove the license and compile the contract.

让我们删除许可证并编译合同。

Our contract is compiled successfully, with a warning that the license is missing.

我们的合同已成功编译，但警告说许可证丢失。

Second, the compiler doesn’t recognize or verify the license. Let's put some random license name and compile to see if it works perfectly.

其次，编译器无法识别或验证许可证。让我们放一些随机的许可证名称并编译，看看它是否完美。

And yes! Our code is compiled successfully.

是的！我们的代码已成功编译。

Third, the license comment is recognized by the compiler anywhere in the file at the file level, but it is recommended to put it at the top of the file.

第三，编译器可以在文件级别的文件中的任何位置识别许可证注释，但建议将其放在文件的顶部。

Let’s put it below the second line and compile.

让我们把它放在第二行下面并编译。

It works perfectly!

它工作得很好！

Now, let's put it at the end of the file. It is showing a warning that the license is missing, which means it should be at least above the last contract. Thus, it is recommended to put it at the top of the file.

现在，让我们把它放在文件的末尾。它显示了一个警告，即许可证丢失，这意味着它至少应该高于最后一份合同。因此，建议将其放在文件的顶部。

Finally, if you do not want to specify a license or if the source code is not open-source, you can write unlicensed.

最后，如果你不想指定许可证，或者源代码不是开源的，你可以在没有许可证的情况下编写。

The important thing to note here is that putting a license is not a mandatory condition in the smart contract structure.

这里需要注意的重要一点是，在智能合约结构中，授予许可证不是强制性条件。

Moving on, the next part is very important!

继续，下一部分非常重要！

This is the part where you have to write the Solidity version that your contract is written in.

这是您必须编写合同所用的Solidity版本的部分。

Pragma Solidity keyword, after that, you have to mention the solidity version. Here we are putting 0.8.23 and then a semicolon.

Pragma Solidity关键字，之后，你必须提到Solidity版本。这里我们先放0.8.23，然后放一个分号。

It indicates that the code is written for Solidity version 0.8.23 and above.

这表明该代码是为Solidity 0.8.23及以上版本编写的。

I know we never had to write it in other programming languages, so let's answer the important question: why write versions?

我知道我们从来没有用其他编程语言编写过它，所以让我们回答一个重要的问题：为什么要编写版本？

To put it simply, it is to ensure compatibility with the intended compiler. Different Solidity versions introduce new features, fix bugs, and sometimes even break existing code. Specifying the version you need tells the compiler which rules and features your contract expects, preventing compilation errors or unexpected behavior when deployed on decentralized networks.

简单地说，这是为了确保与预期编译器的兼容性。不同的Solidity版本引入了新功能，修复了错误，有时甚至破坏了现有的代码。指定您需要的版本告诉编译器您的合同所需的规则和功能，防止在分散网络上部署时出现编译错误或意外行为。

Let's remove it and compile. Compilation has failed! Thus, unlike SPDX, writing Solidity version is a must. The contract won't compile and deploy if the compiler version is missing.

让我们删除它并编译。编译失败！因此，与SPDX不同，编写Solidity版本是必须的。如果缺少编译器版本，则合约将无法编译和部署。

You can write versions in three ways.

你可以用三种方式编写版本。

First, greater than - This is an example of the greater than type, and

首先，大于-这是大于类型的一个例子，以及

Second is specifying a range of compiler versions,

第二是指定编译器版本的范围，

and third is specifying the exact compiler version.

第三是指定确切的编译器版本。

For the range one, you have to mention the range of compiler versions. For example, here, it specifies that the code is written for the Solidity version greater than 0.8.2 and less than 0.9.0, which means between 0.8.2 and 0.9.0.

对于范围一，你必须提到编译器版本的范围。例如，在这里，它指定代码是为大于0.8.2且小于0.9.0的Solidity版本编写的，这意味着在0.8.2和0.9.0之间。

Now you can write your smart contract. We define a contract with the contract keyword, followed by the name of the contract, and then curly brackets, and done!

现在，您可以编写智能合约。我们用合同关键字定义一个合同，后跟合同名称，然后用花括号，就完成了！

You write all intended code in these brackets.

您可以在这些括号中编写所有预期的代码。

You can create multiple contracts in the file, just keep the names different. Here we got an error because the contract name is the same as above. Let's change it, and yes! It has compiled successfully!

您可以在文件中创建多个合同，只需保持名称不同即可。这里我们遇到了一个错误，因为合约名称与上面的相同。让我们改变它，是的！已成功编译！

So that was all about the smart contract structure. In the next exercise, create a basic smart contract.

这就是智能合约结构。在下一个练习中，创建一个基本的智能合约。