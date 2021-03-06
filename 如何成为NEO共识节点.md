# 如何成为NEO共识节点

> *v1.4 \| [English ver.](How-To-Become-NEO-Consensus-Node.md)*

### **目录**

  * [0. 背景](#0-背景)
      * [现状](#现状)
      * [NEO的流通和治理](#neo的流通和治理)
      * [经济激励](#经济激励)
  * [1. 参选流程](#1-参选流程)
  * [2. 共识节点要求](#2-共识节点要求)
  * [3. 成为合作伙伴(自选)](#3-成为合作伙伴自选)
      * [3.1 发送申请](#31-发送申请)
      * [3.2 测试网运行](#32-测试网运行)
        + [3.2.1 成为候选人](#321-成为候选人)
        + [3.2.2 共识节点运行](#322-共识节点运行)
      * [3.3 NEO Foundation 的选举周期](#33-neo-foundation-的选举周期)
  * [4. 主网参选](#4-主网参选)
    + [4.1 成为候选人](#41-成为候选人)
    + [4.2 参与选举](#42-参与选举)
      - [4.2.0 背景: 投票机制\*](#420-背景-投票机制)
      - [4.2.1 投票](#421-投票)
  * [5. 获得支持](#5-获得支持)
  * [附录1. 用API查询候选人票数](#附录1-用api查询候选人票数)
  * [附录2. 在官网检测页面添加信息](#附录2-在官网检测页面添加信息)



## 0. 背景

### 现状

目前主网的共识节点共有7个 (见[共识节点检测页面](https://neo.org/consensus))：

- NEO Foundation维护 5个
- CityOfZion社区维护1个
- KPN维护1个

目前测试网的共识节点共有7个：

- NEO Foundation维护2个
- NEO Global Development维护1个
- CityOfZion社区维护2个
- KPN维护1个
- Swisscom维护1个

### NEO的流通和治理

NEO 中内置两种原生代币，NEO（缩写符号 NEO）和 NeoGas（缩写符号 GAS）。
NEO 是管理代币，总量 1 亿份，用于实现对 NEO 网络的管理权。管理权包括投票进行记账人选举，NEO 网络参数更改等。NEO 的最小单位为 1，不可再分割。GAS 是燃料代币，最大总量上限为 1 亿，用于实现对 NEO 网络使用时的资源控制。NEO 网络对代币转账和智能合约的运行和存储进行收费，从而实现对记账人的经济激励和防止资源滥用。GAS 的最小单位为 0.00000001。

NEO 的 1 亿管理代币分为两部分，第一部分 5000 万份 NEO 用于按轮次和比例分发给 NEO 开发经费众筹的支持者，该部分已经分发完毕。第二部分 5000 万份由 NEO 理事会管理，用于支持 NEO 网络的长期开发、运维和生态发展。该部分的 NEO 处于锁定期，在 2017 年 10 月 16 日 NEO 网络运行达 1 年时方可解锁被使用。这部分 NEO 不会进入交易所交易，仅用于长期支持 NEO 项目，计划按如下比例分配使用：

🔹 1000 万份（总量 10%）用于激励 NEO 开发者和 NEO Foundation成员

🔹 1000 万份（总量 10%）用于激励 NEO 周边生态开发者

🔹 1500 万份（总量 15%）用于交叉投资其他区块链项目，所获得代币归属于 NEO 理事会，并仅用于 NEO 项目

🔹 1500 万份（总量 15%）机动使用

🔹 每年使用的 NEO 原则上不得超过 1500 万份

根据此计划，NEO预计的解锁时间表如下\*：

| 时间   | 新解锁NEO | 总解锁NEO |
| ---- | ------ | ------ |
| 2016 | 5000 万 | 5000 万 |
| 2017 | 1500 万 | 6500 万 |
| 2018 | 1500 万 | 8000 万 |
| 2019 | 1500 万 | 9500 万 |
| 2020 | 500 万  | 1 亿    |

> *\*: 实际的解锁量以NEO的财务报表为准。*

<a name="on-chain-off-chain"> </a>

虽然NEO致力于建设去中心化的组织架构，但根据NEO的解锁策略，NEO Foundation在未来的几年中会拥有大量票数。因此，NEO现阶段分为两种治理方式，链上治理和链下治理。

#### 链上治理

链上治理依靠NEO区块链本身的机制实现管理，也是NEO期望在未来实现的主要管理方式。

NEO 管理代币的持有人是 NEO 网络的所有者和管理者，通过在 NEO 网络上投票来实现管理权，通过获得 NEO 生成的 GAS 燃料代币来实现 NEO 网络的使用权。 NEO 管理代币可以被转让。

#### 链下治理

链下治理依靠NEO Foundation的持续支持。

在运维共识节点，开发NEO核心项目以及推广和发展NEO生态之外，NEO Foundation持有的票会投给符合要求的战略合作伙伴，促进NEO生态的发展。

### 经济激励

NEO网络的激励模型正在讨论中。计划将节点使用网络资源时收取的GAS燃料费分发给共识节点。

本节将在激励模型确认后给予更新。

## 1. 参选流程

NEO的治理分为两部分，线上治理和线下治理，对于不同的治理方法，申请流程有所不同。关于两种参选方式的区别，相见上一章的<a href="#user-content-on-chain-off-chain">相关内容</a>。 

**1) 链上治理申请人**

如果想要利用链上治理的机制，独立运维共识节点，从NEO持有者获得投票，步骤如下：

- [2.共识节点要求](#2-共识节点要求)
- [4.主网参选](#4-主网参选)
- [5.获得支持](5-获得支持)

**2) 链下治理申请人**

如果想要与NEO Foundation建立战略合作关系(链下治理)，并获得NEO Foundation的投票，步骤如下：

- [2.共识节点要求](#2-共识节点要求)
- [3. 成为合作伙伴](#3-成为合作伙伴自选)
- [4.主网参选](#4-主网参选)
- [5.获得支持](#5-获得支持)



## 2. 共识节点要求

> **适用于链上治理和链下治理申请人**

[所有](#参选人性质)节点候选人或者组织应向社区提供以下信息，信息可以发布于NEO官网的[投票检测页面](#附录2-在官网检测页面添加信息)里，并发布在组织官网上。（以下列表仅供参考）

- 公共网站，社交账号
- 联系方式(邮箱，Discord账号等)
- 组织名称，总部位置
- 服务器类型，服务器配置团队名单及2/3的团队成员图片及背景
- 技术方案(安全，维护，长期稳定性， 容灾备份)，维护人员以及预算
- 硬件扩容计划
- 对NEO生态的贡献

服务器参考最低配置：

- 4核处理器
- 8G内存
- 10M带宽
- 100G SSD硬盘


## 3. 成为合作伙伴(自选)

### 3.1 发送申请

> **只适用于链下治理申请人；链上治理申请人见 [3. 主网运行](#3-主网运行)**

[链下治理](#参选人性质)申请人可将自己的组织信息和运维提案通过邮件发送到

consensus@neo.org

建议提案中包括["1. 共识节点要求"](#1-共识节点要求)里列举的信息。NEO Foundation会讨论申请者提供的条件是否符合要求。

申请结果会通过邮件反馈给申请人或组织。审核未通过的补充缺少信息，提升配置和完善相应的方案再提交审核。

### 3.2 测试网运行

[链下治理](#参选人性质)申请人在申请成功后首先需要试运行测试网的共识节点。试运行6个月后，则可转入主网运行。

要成为测试网的共识节点，需要先在测试网上注册为候选人。

#### 3.2.1 成为候选人

> *在测试网和主网成为候选节点的步骤完全相同，唯一区别取决于客户端连接的是哪一个链。关于主网和测试网的切换，请参阅[此文档](http://docs.neo.org/zh-cn/network/testnet.html)*

1. 在 NEO-GUI 中，打开要报名候选人的钱包账户。

2. 点击 `高级` -> `选举`。

3. 选取该地址公钥，点击 `确定`。注意此操作将花费 1000 GAS。完成后会显示交易构造成功提示以及交易ID。

   <img src="https://raw.githubusercontent.com/taomo-eo/docs/master/Becoming_Consensus_Node/img/candidate.png" width="725">

4. 如果看到交易构造成功提示，那么这个账号就成功成为了候选人。可以通过API`getvalidators`方法来查询所有候选人以及候选人得票数。([见附录1](#附录1-用api查询候选人票数))

#### 3.2.2 共识节点运行

注册完成后NEO Foundation将会给投票给此节点，使其成为共识节点。

测试网运行期间，如果存在问题则申请方需要积极配合解决，NGD术人员会提供支持。

测试网运行6个月之后，则可转入主网运行。

### 3.3 NEO Foundation 的选举周期

NEO Foundation计划从2018年11月30日起，每隔三个月设为一个选举周期。Foundation根据候选人对NEO生态的帮助程度在每个选举周期尽可能选出一个节点。每一轮未选上的申请者会自动加入下轮选举池中。当7个节点完全去中心化后，NEO Foundation会在新的选举周期决定是否新增共识节点。

以下是2019年的选举周期:

- 2018年11月30日 - 2019年2月28日
- 2019年2月28日 - 2019年5月31日
- 2019年5月31日 - 2019年8月31日
- 2019年8月31日 - 2019年11月30日

## 4. 主网参选

> **适用于链上治理和链下治理申请人**

[所有](#参选人性质)节点候选人要想参与主网选举并成为共识节点，需要以下步骤：

### 4.1 成为候选人

用GUI连接到主网，重复[2.2.1 成为候选人](#221-成为候选人)的步骤。

### 4.2 参与选举 

#### 4.2.0 背景: 投票机制\*

> *\*: NEO3.0 对投票机制会进行更新。届时此文档也会做相应更新。*

每个 NEO 节点都可以对候选人进行投票，当前投票账户中的 NEO 数量会自动计算为所投候选人的票数，当投票给多位候选人时，每位候选人都将获得与当前投票账户中 NEO 数量相等的票数。例如当前账户有 100 个 NEO，从该账户投票给三位候选人，则每位候选人得到 100 票。投票后如果花费了该账户的 NEO，则候选人的票数也将实时更改为当前账户 NEO 余额数。

投票后，NEO 网络将根据每个账户所投候选人数进行实时计算，选出共识节点。计算方法为：

1. 对每个账户所投候选人数按大小排序，得到数组 C1, C2, ..., Cn
2. 去掉数组中前 25% 和后 25% 的数值
3. 对剩余的 50% 数值进行加权平均，得出 NEO 共识节点数 N
4. 选出得票数最高的前 N 名候选人成为共识节点

#### 4.2.1 投票

> **适用于共识节点申请人以及所有NEO持有者**

任何持有NEO的节点都可以在GUI上进行投票。候选节点的运维者可以给自己的节点投票。

1. 在 NEO-GUI 中，打开要投票的钱包账户。

2. 右键点击该账户 -> `投票`。在候选人框内输入要投票的候选人公钥，换行可以输入多个公钥，但注意每行不能包含空格，如下图所示：

   <img src="https://raw.githubusercontent.com/taomo-eo/docs/master/Becoming_Consensus_Node/img/votemulti.png" width="650">

   *例：给7个候选人各投等同于NEO数量(1)的票*

3. 如果看到交易构造成功提示，投票就已经成功。可以在官网的投票检测页面或通过API来查询所有候选人以及候选人得票数。([见附录1](#附录1-用api查询候选人票数))

## 5 获得支持

> **适用于链上治理和链下治理申请人**

确认节点在区块链上注册为候选人后, 与NEO建立了合作关系的链下治理申请人在参选时会得到NEO Foundation的投票。

对于链上治理申请人，获得社区的了解和支持会提升社区里的NEO持有者给候选人投票的可能性。建议使用以下几种方法：

- 在neo.org的[投票检测页面](http://neo.org/consensusSited)添加候选人的各类信息 。具体步骤见[附录2](#附录2-在官网检测页面添加信息) 


- 在自己的组织官网上展示NEO节点竞选的相关信息
- 通过NEO社区和社交媒体推广

*如果在主网参选获得足够的投票，就能成为主网共识节点。*

---

## 附录1. 用API查询候选人票数

如果想要查询候选人名单和票数，可以使用Postman或任何其他RPC程序调用API来查询。(json-RPC调用API的具体步骤可[见此文档](使用RPC调用NEO%20API.md))

如下图所示，调用`getvalidators`方法。

<img src="https://raw.githubusercontent.com/taomo-eo/docs/master/Becoming_Consensus_Node/img/getvalidator2.png" width="725">

可以查看到返回的响应正文中显示出该公钥与对应的的票数。

图片中，余额为 100000000 的账户投票给了公钥为`3076fc0ee6c6ccf3fb0c9b3ff9d0e3d9ba7ef97e54c77240991ec1dffa295503b`的候选人。

### 分辨共识节点

在API返回的json文件里，**`active`** 这一项的值代表此节点的状态。

`false`表示此节点是候选节点

`true`表示此节点是共识节点



## 附录2. 在官网检测页面添加信息

[投票检测页面](https://neo.org/consensusSited)可用来检测所有主网候选节点的状态和票数。以及添加候选节点的信息。<img src="https://raw.githubusercontent.com/taomo-eo/docs/master/Becoming_Consensus_Node/img/consensusSited1a.png" width="755">

**要添加信息：**

1. 在页面中点击“竞选节点”旁的 <img src="https://raw.githubusercontent.com/taomo-eo/docs/master/Becoming_Consensus_Node/img/consensusSited2a.png" width="155">，进入信息填写框。

2. 在“公钥”列表中选择候选人的公钥，填写相关信息。

3. 点击“生成散列值”，并复制生成的字符串。

   <img src="https://raw.githubusercontent.com/taomo-eo/docs/master/Becoming_Consensus_Node/img/consensusSited3a.png" width="620">

4. 在 NEO-GUI 客户端中，点击“高级”-> “消息签名”。

   <img src="https://raw.githubusercontent.com/taomo-eo/docs/master/Becoming_Consensus_Node/img/consensusSite4.png" width="725">

5. 在“地址”中选择候选人公钥对应的账户地址，在“输入”框中填入之前生成的字符串，点击“签名”。
   “输出”框中显示出对应的签名，将其复制。

   <img src="https://raw.githubusercontent.com/taomo-eo/docs/master/Becoming_Consensus_Node/img/consensusSite5.png" width="725">

6. 回到填写候选人信息框，将获取到的签名填入，并点击“提交”

   <img src="https://raw.githubusercontent.com/taomo-eo/docs/master/Becoming_Consensus_Node/img/consensusSited6a.png" width="620">

   将看到该候选节点所在行的下拉箭头激活为绿色，可点击箭头扩展显示详细信息。
