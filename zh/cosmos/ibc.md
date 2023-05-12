---
order: 3
---

# IBC

## 如何理解跨链协议 IBC？

IBC 是 Cosmos 围绕 Cosmos 网络 和 Tendermint 共识 而设计的 跨链通信协议 ，也就是 Inter Blockchain Communication 跨链通讯协议 ，用于 Hub 与 Zone 之间互通的双向通信，以进行 协议层 的价值 跨链传递 。IBC利用Tendermint共识的即时最终确定性属性（尽管它可以与任何“快速确定性”区块链引擎一起使用），以允许异构链相互传递价值（即令牌）或数据。

## 什么是异构链？

从本质上讲，它可以归结为两点：

**不同的层：**异构链具有不同的层，这意味着它们在实现网络，共识和应用程序部分的方式上可能有所不同。为了与IBC兼容，区块链只需要遵循一些要求，主要的是共识层必须具有快速的确定性。工作量证明链（如比特币和以太坊）不属于此类，因为它们具有概率确定性。

**主权：**每个区块链均由一组验证器维护，这些验证器的工作是就下一个区块提交区块链达成协议。在工作量证明区块链中，这些验证器称为矿工。主权区块链是具有自己的验证器集的区块链。在许多情况下，重要的是让区块链拥有主权，因为验证者最终负责修改状态。在以太坊中，所有应用程序都由一组通用的验证器运行。因此，每个申请仅具有有限的主权。

IBC允许异构区块链彼此之间传递令牌和数据，这意味着具有不同应用程序和验证器集的区块链可以互操作。例如，它允许公共和私有区块链相互之间交换令牌。当前，没有其他区块链框架支持这种级别的互操作性。

## IBC如何运作

IBC背后的原理非常简单。让我们以一个示例为例，链A上的一个帐户要发送10个令牌（让我们称它们为原子）到B链。

**追踪**

连续地，链B接收链A的标题，反之亦然。这允许每个链跟踪另一个链的验证器集。本质上，每个链条都运行一个轻客户 其他的。

**粘接**

启动IBC传输后，ATOM被锁定（保税区）在链A上。 IBC如何运作＃1

**证明继电器**

然后，将10个ATOM绑定的证明从链A中继到链B。 IBC如何运作＃2

**验证方式**

在链B上对照链A的标头验证该证明，如果有效，则在链B上创建10个ATOM凭证。 

请注意，在链B上创建的ATOM不是真正的ATOM，因为ATOM仅存在于链A上。它们是链A上ATOM的B上的表示形式，以及这些ATOM冻结在链A上的证明。