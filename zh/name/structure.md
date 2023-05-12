---
order: 6
---

# 区块链层级结构


## 数据层/ Data Layer

数据层主要描述区块链的物理形式，是区块链上从创世区块起始的链式结构，包含了区块链的区块数据、链式结构以及区块上的随机数、时间戳、公私钥数据等，是整个区块链技术中最底层的数据结构。

## 网络层/ Network Layer

网络层主要通过 P2P 技术实现分布式网络的机制，网络层包括 P2P 组网机制、数据传播机制和数据验证机制，因此区块链本质上是一个 P2P 的网络，具备自动组网的机制，节点之间通过维护一个共同的区块链结构来保持通信。

## 共识层/ Consensus Layer

共识层主要包含共识算法以及共识机制，能让高度分散的节点在去中心化的区块链网络中高效地针对区块数据的有效性达成共识，是区块链的核心技术之一，也是区块链社群的治理机制。目前至少有数十种共识机制算法，包含工作量证明、权益证明、权益授权证明、燃烧证明、重要性证明等。

*数据层、网络层、共识层是构建区块链技术的必要元素，缺少任何一层都不能称之为真正意义上的区块链技术。*

## 激励层/ Actuator Layer

激励层主要包括经济激励的发行制度和分配制度，其功能是提供一定的激励措施，鼓励节点参与区块链中安全验证工作，并将经济因素纳入到区块链技术体系中，激励遵守规则参与记账的节点，并惩罚不遵守规则的节点。

## 合约层/ Contract Layer

合约层主要包括各种脚本、代码、算法机制及智能合约，是区块链可编程的基础。将代码嵌入区块链或是令牌中，实现可以自定义的智能合约，并在达到某个确定的约束条件的情况下，无需经由第三方就能够自动执行，是区块链去信任的基础。

## 应用层/ Application Layer

区块链的应用层封装了各种应用场景和案例，类似于电脑操作系统上的应用程序、互联网浏览器上的门户网站、搜寻引擎、电子商城或是手机端上的用部署在如以太坊、EOS、OTUM、上并在现实生活场景中落地。未来的可编程金融和可编程社会也将会是搭建在应用层上。

*激励层、合约层和应用层不是每个区块链应用的必要因素，一些区块链应用并不完整包含此三层结构。*