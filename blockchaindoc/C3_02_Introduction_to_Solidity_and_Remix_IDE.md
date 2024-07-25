Hello and welcome back, in this chapter, we will discuss more about solidity programming language, and development tools that are used to learn, build, and test solidity.

大家好，欢迎回来，在本章中，我们将更多地讨论solidity编程语言，以及用于学习、构建和测试solidity的开发工具。

Programming languages are really important in software development because they give us a structured and standardized way to talk to computers.

编程语言在软件开发中非常重要，因为它们为我们提供了一种结构化和标准化的与计算机对话的方式。

They enable developers to write code, create applications, and solve complex problems.

它们使开发人员能够编写代码、创建应用程序和解决复杂问题。

Each programming language has its own unique features and is well-suited for specific tasks, giving developers the freedom to choose the language that best fits their requirements and desired outcomes.

每种编程语言都有其独特的功能，非常适合特定的任务，让开发人员可以自由选择最适合他们的要求和期望结果的语言。

Let's discuss this with examples. JavaScript is mainly used to develop web applications, in conjunction with HTML and CSS.

让我们用例子来讨论这个问题。JavaScript主要用于开发web应用程序，与HTML和CSS结合使用。

Python and R are primarily used in data science. Similarly, C or C++ is used in developing embedded system programs.

Python和R主要用于数据科学。同样，C或C++用于开发嵌入式系统程序。

The examples I am giving do not imply that a particular language is limited to that domain only; these languages can be used in other domains as well. However, they are widely used in their specific domains.

我给出的例子并不意味着特定语言仅限于该领域；这些语言也可以用于其他领域。然而，它们在其特定领域中被广泛使用。

Similar to the above languages, Solidity is also one of the programming languages that is mainly used to develop smart contracts programs.

与上述语言类似，Solidity也是主要用于开发智能合约程序的编程语言之一。

You can consider a smart contract to be a self-executing contract directly written into the code. It is just a computer program.

您可以将智能合约视为直接写入代码的自动执行合约。它只是一个计算机程序。

This program is then stored and executed on the blockchain, like Ethereum.

然后，该程序在区块链上存储和执行，就像以太坊一样。

and Since the program is on the blockchain, it automatically receives all the benefits of the blockchain, such as transparency, immutability, security, and decentralization.

由于该程序位于区块链上，它会自动获得区块链的所有好处，如透明度、不变性、安全性和去中心化。

We will see how to build a smart contract and deploy it on the blockchain platforms as we proceed in this course.

在本课程中，我们将了解如何构建智能合约并将其部署在区块链平台上。

I hope you have got some understanding of where the solidity programming is used.

我希望您已经了解了solidity编程在哪里使用。

Now to develop any programming language we need a tool where we can run the code, test and debug it right? For that, we have a Remix IDE.

现在，要开发任何编程语言，我们需要一个工具来运行代码、测试和调试它，对吗？为此，我们有一个Remix IDE。

Now let’s discuss the remix IDE.

现在让我们讨论一下混音IDE。

Remix IDE is an integrated development environment specifically designed for developing and testing Solidity smart contracts.

Remix IDE是一个专门为开发和测试Solidity智能合约而设计的集成开发环境。

Similar It provides a user-friendly interface that allows developers to write, compile, deploy, and interact with smart contracts directly from the browser.

SimilarIt提供了一个用户友好的界面，允许开发人员直接从浏览器编写、编译、部署智能合约并与之交互。

So, this is how the remix IDE looks.

这就是混音IDE的样子。

There are 3 main sections as you can see on the left side panel.

您可以在左侧面板上看到三个主要部分。

The first one is the files section, this is where we can create and manage files and folders. We can also create different workspaces.

第一个是文件部分，我们可以在这里创建和管理文件和文件夹。我们还可以创建不同的工作空间。

As you can see we have some icons here to interact with the file, with the first one we can create a new file, and with this one we can create a new folder, and with this we can publish all of our code to GitHub, next one is used to upload any local file here in the remix and the last one is to upload a folder.

正如你所看到的，我们在这里有一些图标可以与文件交互，第一个图标可以创建一个新文件，第二个图标可以新建一个文件夹，然后我们可以将所有代码发布到GitHub，第三个图标用于在混音中上传任何本地文件，最后一个图标用于上传一个文件夹。

At the top here in the menu, you can see different options to create, clone and backup restore workspace files and folders.

在菜单的顶部，您可以看到创建、克隆和备份还原工作区文件和文件夹的不同选项。

The next section is compile, this is the inbuilt solidity compiler where we can compile our code.

下一节是编译，这是一个内置的solidity编译器，我们可以在其中编译代码。

Compiling is the process of converting human-readable code written in a programming language into machine-readable code that can be executed by a computer as simple as that.

编译是将用编程语言编写的人类可读代码转换为机器可读代码的过程，这些代码可以由简单的计算机执行。

from here we can select different versions of the compiler.

从这里我们可以选择不同版本的编译器。

let me just select the sample file from the files and come back here. You can see we have compiled the contract successfully.

让我从文件中选择示例文件，然后回到这里。你可以看到我们已经成功地编写了合约。

And down here you can find the A-B-I and bytecode.

在这里，你可以找到A-B-I和字节码。

A-B-I stands for Application Binary Interface.

A-B-I代表应用程序二进制接口。

The A-B-I includes information such as function names, argument types, and return types.

A-B-I包括函数名、参数类型和返回类型等信息。

When the contract is deployed on the blockchain this a-b-i is used to interact with smart contracts from external applications or other contracts.

当合约部署在区块链上时，a-b-i用于与来自外部应用程序或其他合约的智能合约进行交互。

Bytecode is the compiled form of the Solidity smart contract. It is a low-level representation of the contract that can be executed by the Ethereum Virtual Machine.

Bytecode是Solidity智能合约的编译形式。它是可以由以太坊虚拟机执行的合约的低级表示。

Now, the next section is the "Deploy and Run Transaction" section. This section is used to deploy the smart contract and interact with its functions.

现在，下一节是“部署和运行事务”部分。本节用于部署智能合约并与其功能进行交互。

The first option is to select the environment. There are different environments in which we can deploy our smart contract.

第一种选择是选择环境。我们可以在不同的环境中部署智能合约。

For example, if you want to test your smart contract, you will want to deploy it on the test blockchain network first before directly deploying it on the main blockchain network.

例如，如果你想测试你的智能合约，你需要先在测试区块链网络上部署它，然后再直接部署到主区块链网络。

So, we have multiple options here.

所以，我们有多种选择。

The next one is accounts. Remix IDE provides various accounts with pre-existing test account balances to test the smart contract. The next one is to set the gas limit and value. We will see this later.

下一个是账目。Remix IDE为各种帐户提供预先存在的测试帐户余额，以测试智能合约。下一步是设置气体限制和值。我们稍后会看到这一点。

And then, select the smart contract that we want to deploy and hit the deploy button.

然后，选择我们要部署的智能合约并点击部署按钮。

Once deployed, you can see we have an interactive button over here.

部署后，您可以看到我们在这里有一个交互式按钮。

These buttons specify the functions that are declared in the smart contract. Right now, this is the storage smart contract which can be used to store the number on the blockchain and then retrieve it back.

这些按钮指定了智能合约中声明的功能。现在，这是存储智能合约，可用于将数字存储在区块链上，然后将其检索回来。

Let's store some number and check if it's working perfectly or not.

让我们存储一些数字，检查它是否正常工作。

Apart from the Remix IDE, there are various tools like Hardhat, which is a complete framework to write tests, debug, and deploy any smart contracts.

除了Remix IDE，还有各种工具，如Hardhat，它是一个完整的框架，可以编写测试、调试和部署任何智能合约。

We will learn Hardhat in some other course. In this course, we will mostly use the Remix IDE only.

我们将在其他课程中学习Hardhat。在本课程中，我们将主要只使用Remix IDE。

So, that was all about Solidity and its development tools. In the next chapter, let's discuss the smart contract structure.

所以，这就是Solidity及其开发工具的全部内容。在下一章中，让我们讨论一下智能合约结构。

See you in the next chapter.

下一章见。