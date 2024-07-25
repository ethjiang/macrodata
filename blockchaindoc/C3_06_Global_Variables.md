## Global Variables
Hello and welcome back, I hope you have completed the exercise successfully and you now understand the functions in smart contracts. In this chapter, we will discuss the various data types that are available in the solidity.

大家好，欢迎回来，我希望您已经成功完成了练习，现在您已经了解了智能合约中的功能。在本章中，我们将讨论solidity中可用的各种数据类型。

## Overview
Solidity have special variables that you will use very often while building smart contracts. Let's discuss them one by one.

Solidity具有特殊的变量，您在构建智能合约时会经常使用这些变量。让我们逐一讨论一下。

## msg.sender
In Solidity, msg.sender is a global variable that represents the address of the account (or contract) that is currently interacting with the smart contract. It refers to the sender of the transaction that triggered the execution of the current function or contract.

在Solidity中，msg.sender是一个全局变量，表示当前与智能合约交互的帐户（或合约）的地址。它指的是触发当前功能或合约执行的交易的发送方。

msg.sender in Solidity is like a signature on a letter. When someone interacts with a smart contract on the Ethereum blockchain, msg.sender tells the contract who that someone is. It helps the contract know who is sending a message or asking it to do something.

Solidity中的msg.sender就像信件上的签名。当有人在以太坊区块链上与智能合约交互时，msg.sender告诉合约是谁。这有助于合约知道是谁在发送消息或要求它做什么。

```agsl
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SenderContract {
    // Function to get the address of the sender
    function getSender() public view returns (address) {
        return msg.sender;
    }
}
```

So, when you deploy the above contract in Remix, and call the getSender() function, you will receive the address which is selected in the remix accounts.

因此，当您在Remix中部署上述合约并调用getSender（）函数时，您将收到在混音帐户中选择的地址。

## msg.value
In Solidity, a contract can indeed hold Ether, the native cryptocurrency of the Ethereum blockchain. When someone sends Ether to a contract, it's not stored in the same way as in a regular Ethereum address; rather, it becomes part of the contract's balance. This balance can be manipulated and managed by the contract's code.

在Solidity中，合约确实可以持有以太坊区块链的原生加密货币Ether。当有人向合约发送以太币时，它的存储方式与常规以太坊地址不同；相反，它成为了合同平衡的一部分。这种平衡可以通过合同的代码来操纵和管理。

Here's a brief explanation:

以下是一个简短的解释：

Ether in Contracts: Just like regular Ethereum addresses, contracts have a balance denominated in Ether. When someone sends Ether to a contract, the contract's balance increases.

合约中的以太币：就像普通的以太坊地址一样，合约也有以以太币计价的余额。当有人向合约发送以太币时，合约的余额会增加。

msg.value: msg.value is a special variable in Solidity that represents the amount of Ether (in Wei) sent along with a function call or transaction. It tells the contract how much Ether was included in the transaction. Wei is the smallest unit of Ether, where 1 Ether is equivalent to 10^18 Wei.

msg.value:msg.value是Solidity中的一个特殊变量，表示随函数调用或事务一起发送的以太币量（Wei）。它告诉合同交易中包含了多少以太币。Wei是Ether的最小单位，其中1 Ether等于10^18 Wei。

Here's a simple example demonstrating how a contract can receive and manage Ether:

以下是一个简单的示例，演示合约如何接收和管理以太币：

```agsl
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract EtherReceiver {
    // This event is emitted when Ether is received
    event Received(address indexed sender, uint256 amount);

    // Function to receive Ether
    receive() external payable {
        // Emit an event to log the received Ether and sender's address
        emit Received(msg.sender, msg.value);
    }

    // Function to get the contract's current balance
    function getBalance() public view returns (uint256) {
        return address(this).balance;
    }
}
```

The receive function is a special function that is automatically called when Ether is sent to the contract. It emits an event to log the sender's address and the amount of Ether sent.

接收函数是一个特殊的函数，当以太币被发送到合约时会自动调用。它发出一个事件来记录发送者的地址和发送的以太币数量。

The getBalance function allows you to check the contract's current Ether balance. You can send the ether tokens from the remix ide by adding the value in the "value" box below accounts list.

getBalance函数允许您检查合约的当前以太币余额。您可以通过在帐户列表下方的“值”框中添加值来从混音器发送以太代币。

## Transfer function
In Solidity, the transfer function is a method available for sending Ether (the native cryptocurrency of the Ethereum blockchain) from one address to another. It's commonly used for transferring funds between accounts within a smart contract. The transfer function is a safer alternative to direct Ether transfers because it includes a limited amount of gas to prevent reentrancy attacks and other potential issues.

在Solidity中，转移函数是一种将以太币（以太坊区块链的原生加密货币）从一个地址发送到另一个地址的方法。它通常用于在智能合约中的账户之间转移资金。传递函数是直接以太币传递的一种更安全的替代方案，因为它包含有限量的气体，以防止重入攻击和其他潜在问题。

Here's a simple example using the transfer function:

下面是一个使用传递函数的简单示例：

```agsl
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract EtherTransferExample {
    // Function to transfer Ether to a specified recipient
    function sendEther(address payable recipient) external payable {
        // Using require to ensure a valid recipient address is provided
        require(recipient != address(0), "Invalid recipient address");
        
        // Using transfer function to send Ether to the specified recipient
        recipient.transfer(msg.value);
    }
}
```

The sendEther function now takes an additional parameter address payable recipient as an argument.

sendEther函数现在接受一个额外的参数address payable recipient作为参数。

The require statement checks that the provided recipient address is not zero (0x0 or address(0)), ensuring a valid recipient is specified.

require语句检查提供的收件人地址是否不为零（0x0或地址（0）），以确保指定了有效的收件人。

The recipient parameter is marked as payable to allow it to receive Ether.

接收者参数被标记为应付，以允许其接收以太币。

Apart from the above variables, solidity offers a wide range of global variables, In the next chapter, there is a complete list of all available solidity variables. See you in the next chapter.

除了上述变量外，solidity还提供了广泛的全局变量。在下一章中，将提供所有可用solidity变量的完整列表。下一章见。