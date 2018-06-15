![Metronome](img/logo.png)

版本 0.986（上次更新时间 2018 年 5 月 30 日）

**注释：**

\(1) 本用户手册介绍一种新型加密货币 Metronome 的设计和结构，草稿仍在持续更新中。Metronome 及其基础技术仍处于开发阶段，本用户手册将在整个过程中更新以反映整个开发周期的变化。为了确保材料的准确性，已采取各种措施，但 Metronome 创始人及其合作伙伴不保证本用户手册中材料的准确性或完整性。

\(2) Metronome 的潜在买方和 Metronome 生态系统的参与者应阅读本用户手册，其中包括附录 \[A\] 中的确认和免责声明，并且在购买之前应仔细考虑所有风险。

**用户手册许可**

© 2018 Autonomous Software 版权所有。保留未经许可方
明确授予的所有权利。

AUTONOMOUS SOFTWARE（“许可方”）拥有并保留本“Metronome 用户手册”（以下简称“用户手册”）和通用版本（定义如下）的排他性所有权，以及全部权利、所有权、全部版权和其他知识产权。用户手册和通用版本统称为“工作”。

“METRONOME”、“MET”和 METRONOME 徽标（统称为“METRONOME 标志”）是许可方的商标，仅在许可方明确书面许可的情况下才能使用。您不得在任何产品或服务上或以任何其他方式使用 METRONOME 标志或任何类似标志，这可能在市场上导致混淆，包括在广告中或在软件及硬件中。

1. **许可授予和限制。**根据本许可协议的条款和
条件，许可方在此授予您全球范围的、
免版税、非独占、永久许可，以复制、展示和
发行整个用户手册（不允许部分发行），不得
修改、调整或创建通用的衍生
版本（定义如下），以及复制、展示和发行此类作品；
前提条件是上述内容均不能暗示您
或您的工作或加密货币、智能合约或
技术与许可方或其附属机构有任何方式的关联或
认可。上述权利可在
所有媒体和形式中行使，无论是现在已知的还是此后
设计出来的。上述权利包括进行技术上必要的
修改以便
其他媒体和形式行使权利。每次您发行或公开
执行工作时，许可方都会按照与本许可中授予
您的许可，以相同的条款和条件向
工作授予工作许可。“通用版本”是指不包括或包含任何
许可方、许可方附属公司或 Metronome、MET 
或任何 Metronome 标志的
用户手册版本。

2. **对用户手册的建议修改。**向用户手册提交任何
修改建议，即表明您同意向
许可方授予所提建议的所有版权，但不限于此类
修改。因此，许可方可以自行决定
在
用户手册（全部或部分，以及修改或未修改的
格式）中是否包括任何此类建议修改。

3. **声明和保证**。用户手册乃按原样提供，如无任何种类、明示、暗示、法定或其他任何形式的声明或保证，包括但不限于对所有权、适销性、特定用途适用性、非侵权性、准确性，或是否存在错误的保证。某些司法管辖区不允许排除暗示性的保证，因此这些排除条款可能不适用于您。

4. **可执行性**。如果本许可的某项条款无效或在适用法律下无法执行，本许可其余条款的有效性或可执行性不受影响，若本协议双方未采取进一步行动，则应将此条款更改为使此类条款有效且可强制执行所必需的最低限度。本许可的任何条款均不得被视为放弃，也不应被视为同意，否则此类放弃或同意应以书面形式签署，并由负责放弃或同意的一方签署。

5. **条约权利**。本许可中所授予的权利以及所引用的主题基于《保护文学和艺术作品伯尔尼公约》（1979 年 9 月 28 日修订）、1961 年《罗马公约》、1996 年《WIPO 版权条约》、1996 年《世界知识产权组织表演和录音制品条约》和《世界版权公约》（1971 年 7 月 24 日修订）。这些权利和主题在相关的司法管辖范围内生效，根据适用的国家/地区法律中有关条约规定的相应条款，要求执行许可条款。如果在适用的版权法中授予的标准权利组别包括本许可下未授予的额外权利，则该等附加权利被视为在许可中包含；本许可并非旨在限制适用法律下任何权利的许可。

目录
=================

**[目录](#table-of-contents)**

**[表格和数字列表](#list-of-tables-and-figures)**

**[动机](#motivations)**

> [真正让加密货币进入下一阶段](#taking-cryptocurrency-to-the-next-level-literally)

**[执行摘要](#executive-summary)**

**[背景](#background)**

> [区块链技术](#blockchain-technology)
>
> [加密货币](#cryptocurrency)
>
> [降价拍卖](#descending-price-auctions)

**[Metronome 简介](#introducing-metronome)**

**[Metronome 工作原理](#how-metronome-works)**

> [跨区块链可迁移性](#cross-blockchain-portability)
>
> [分布式、自愿的共识 > 治理](#distributed-voluntary-consensus-governance)

**[迄今为止的加密货币市场背景](#cryptocurrency-market-context-to-date) **

> [整体布局](#the-landscape)

**[Metronome 合约和技术层面](#metronome-contracts-and-technical-aspects)**

**[Metronome 收益和自治转换合约](#metronome-proceeds-and-autonomous-converter-contracts)**

**[代币供应经济学](#token-supply-economics)**

> [理论](#theory)
>
> [供应时间表](#supply-schedule)
>
> [Metronome 核心](#metronome-core)
>
> [代币 API](#token-api)
>
> [拍卖 API](#auction-api)
>
> [Metronome 收益合约](#metronome-proceeds-contract)
>
> [收益合约 API](#proceeds-contract-api)
>
> [Metronome 自治转换合约](#metronome-autonomous-converter-contract)
>
> [自治转换合约 API](#autonomous-converter-contract-api)
>
> [TokenLocker](#tokenlocker)
>
> [TokenLocker API](#tokenlocker-api)
>
> [TokenPorter](#tokenporter)
>
> [TokenPorter API](#tokenporter-api)

**[合约条款术语表](#glossary-of-contract-terms) **

**[附录 A](#appendix-a) **

表格和数字列表
==========================

图 1：USD 和 BTC 货币基数的比较 11

图 2：Metronome 合约之间的流动和相互作用 12

图 3：跨区块链可迁移性演示 15

图 4：流行的加密货币铸造 18

图 5：比特币和 Metronome 的铸造和供应比较 19

图 6：ZEC 和 MET 创始人保留权益之间的比较 20

表 1：当今加密货币之间的重要属性
比较 21

图 7：自治转换合约的工作原理 22

表 2：供应时间表 27

动机
===========

在 Metronome 的发展过程中，Metronome 创始人渴望从以前的加密货币中汲取教训，建立一个长期货币体系并将此作为唯一目的。考虑到这一点，Metronome 创始人看到了一个新的机会：

- 从经济层面设计出可持久的东西

- 引导去中心化金融产品

- 确保平等取得代币分配

- 确保自治、自治合约

- 真正让加密货币进入下一阶段

**从经济层面设计可持久加密货币**

一些加密货币的铸造或是静态的，或是随着时间的推移逐渐消失，比如比特币[^1][^2]和莱特币[^3]，这让经济学家质疑它们的长期生存能力。[^4][^5]其他加密货币的代币供应在前 ICO 交易中是手工完成的，这些交易给某些人提供了大量的代币供应，导致那些人控制了大多数代币。一些加密货币在预售阶段或私下就已出售给某些人，留给大众的很少。Metronome 试图
通过每日拍卖来解决这些问题。这些拍卖提供了持续代币供应，并且是永久供应。理论上，相对于铸币量要么为零要么趋于零的其他加密货币，持续代币供应提供了可持续性。[^6][^7]Metronome 团队期望这种方式也会鼓励 MET 持有人使用 Metronome 的许多支付功能。那些使用案例实际上是将其用作货币，可能有助于
巩固其耐久性。Metronome 团队还认为，持续铸币也会稀释在给定时间购买的任何潜在的不成比例的金额。Metronome 团队认为自己是在构建一项可持久工程。持久性是 Metronome 的主要目标。

**引导去中心化金融产品**

将去中心化系统导向自我可持续性是一项新的事务，其中的艺术多于科学。Metronome 试图在这里开辟新天地。Metronome 拍卖的所有收益都将纳入两个独立的智能合约，[^8]这些智能合约旨在向可能要出售的 MET 所有者提供流动性。[^9]

鉴于所有拍卖收益都保留在 Metronome 生态系统内，Metronome 团队预计它会蓬勃发展。此外，该团队希望其他人研究 Metronome 的项目和产品模型。

**确保平等取得代币分配**

加密货币应该更加平等。应该有不止 1% 的人可以使用世界上的下一代加密货币。与整个 Metronome 经济相比，向公众广泛发行加密货币可以减少涉众的数量。

降价拍卖旨在以买方认为公平的价格发行代币。[^10]其他 ICO 的代币发行是手工完成的，大多数代币通常在公众得知以前的预售阶段或私下里就已经出售了。[^11]

Metronome 公司在其初始供应拍卖和每日总量批次上都采用了降价拍卖方式，公众可以获得所有拍卖机会。[^12]没有预售、白名单或任何奖金。参与 Metronome 拍卖的每个人都必须按照相同的规则进行操作：以给定价格购买或等待价格下降。在这些公开拍卖中没有人被排除在外或享有特权。[^13]

Metronome 团队认为，初始供应拍卖这种方式可以阻止空间内的大型参与者和其他大型玩家支配 MET 的供应——因为获得不成比例的 MET 数量可能需要支付高于已知的市场价格。该团队还认为，这将鼓励在买方群体中实现更公平的分配。Metronome 并不是为短期投机者寻找一个快速脱手的机会，而是使初始供应拍卖的每个方面都试图提供更公平的 MET 获得和更公平的 
MET 分配。

**自治、自治合约**

人类是容易犯错的。软件和数学在未来数十年及更长的时间内更具可预测性。算法不涉及政治，它不会在人类的自由支配下过度膨胀或操纵货币。有了自治、自治合约，[^14]没有人能根据人的判断力来影响加密货币的价值。为此，Metronome 智能合约的所有权职能将被锁定，以便在发行后无人可以取得它们的所有权。Metronome 采用完全自治方式。

Metronome 被设计为具有自我调节和自治的能力。为此，Metronome 的合约是完全自治的，我们相信在没有创始人干预的情况下，其表现是可预测的。

真正让加密货币进入下一阶段
----------------------------------------------------

其他每种加密货币都只与一个区块链网络相关联。LTC 只记录在莱特币区块链上。BTC 只记录在比特币区块链上。只与一个区块链相关联存在风险：管理不和谐、供应不确定性等。市场不知道跨区块链是可行的，更不用说有需求了。

Metronome 是第一个永远不会只与一个区块链绑定的加密货币。这是第一个可能通过最好的区块链网络获得安全保障的加密货币，并且没有对任何一个区块链的永久承诺。这是一个全新的概念，即使在创新性的加密货币空间中也是如此。

执行摘要
=================

Metronome（“Metronome”或“MET”）是一种新的加密货币，专为拥有机构级的耐久性而设计。Metronome 汲取了其他加密货币（如比特币和以太坊）的经验，其设计可适应未来 100 年甚至更长时间。

Metronome 将以平等的机会向公众发行。Metronome 在发行后创始人将拥有零特权，并且具有高度可预测和可靠的代币供应。

Metronome 代币供应：

- 1 千万个初始 MET 代币供应

   - 8 百万个通过公开降价拍卖发行，详情如下

   - 2 百万个被分配给创始人由创始人持有（20%）

      - 根据特殊 TokenLocker 合约铸币（见 API 部分）

         - 在初始供应拍卖结束时，25% 可供创始人使用

         - 剩余的 75% 以等量分 12 个月获得

         - 只有 Metronome 的创始人才能撤销他们的 TokenLocker 合约，并且只能在上述特定时间撤销

- 每日铸造新的 MET

   - 每日铸造的 MET 通过公开降价拍卖发行

   - 每日铸币量：(i) 每天 2880 个 MET 代币，或 (ii) 相当于每年当时未清偿 MET 代币供应 2.0000% 的年产率

Metronome 的三个核心设计原则是自治、可靠性和可迁移性。它们使 Metronome 独特而持久。

- **自治**

   - 在发行后，没有任何不当的创始人影响——由智能合约自治管理

   - 抵抗个人或社区不相容、分歧或曲解

   - 公众可获得所有销售机会

   - 100% 链上、去中心化、可审计

   - 通过降价拍卖定价

- **可靠**

   - 可预测的代币供应

   - 每天永远以下列两者的较大者铸造新的 MET：(i) 每天 2880 个 MET 代币，或 (ii) 相当于每年当时未清偿 MET 代币供应 2.0000% 的年产率

   - 稳定、可预测的新代币永远供应铸造

   - 设计为可预测的价格

- **可迁移性**

   - 跨区块链可迁移性能实现从不同合约或不同区块链的可证明导出和导入
      - 深层保护加密货币免受治理问题和不稳定因素的影响

   - 新区块链导出和导入功能的社区开发

   - 随着分类账技术平台的成熟，实现向未来区块链的迁移路径

- **其他特性**

   - 初始付款预计将在 15 到 30 秒内结算——结算时间基于底层区块链

   - 批量支付——允许同批发送多笔付款

   - 预订——允许用户之间的定期付款

   - ERC20 符合其他定制功能

在本文件中，我们认为 Metronome 作为一种新的加密货币，它独一无二地满足了上述标准，是世界上第一个自治的、跨区块链加密货币。我们预计，加密货币和其他代币社区将针对这种情况重新设计自己的代币使用方式。

为了实现这一目的和实现自我治理，Metronome 的创始人在初始拍卖之后对 Metronome 代币没有任何特权。Metronome 公司将采用降价拍卖的方式进行初始拍卖和每日总量批次，以使买方有机会以他们认为公平的价格购买。

背景
==========

区块链技术
---------------------

区块链是一种新型的加密安全记录技术，在金融领域有着重要的影响。它是一种分布式的、通常是去中心化的分类账，适用于其整个生态系统中的所有单元。在整个网络中，公共和完整的分类帐需要同步并相互一致。这些被称为节点。节点可以防止区块链单元的“双重支出”，也可以验证网络块中的交易。

块是打包的交易数据、前一个块的散列、目标散列以及一个称为随机数的数字。在节点验证这些块的地方，矿工尝试发现一个使得块中所有数据的散列符合其目标散列的随机数，从而将它们写入区块链。矿工付出了努力和计算能力，会因此得到新铸造的加密货币单位作为奖励。

区块链的“链”指的是矿工为去中心化公共分类账所写的不间断的矿块线。矿工必须将之前区块的数据整合起来，才能成功地发现新的区块，从而将可追溯的历史记录到加密货币的最开始。

加密货币
--------------

加密货币是一种数字货币，它使用加密技术来调节市场中新增的货币供应。通常，成功发现上述挖掘过程中的块后，以新发行加密货币作为奖励。密码学还验证了资金转手的有效性。只有交易用户持有的私钥才能为用户钱包之间的资金转移提供授权。由于这些交易在区块链上是可见的（见上文），并且使用加密密钥确保用户打算发送资金并有足够的资金进行交易，因此，凭借第三方来转移和验证账户之间资金转移的需求减少了。加密技术取代了
清算所和其他中介机构的角色。因此，加密货币有可能为货币供应和法定货币发行提供更大的可预测性。

法定货币的发行和供应可以由发行机构进行多方面管理，而加密货币的行为必定符合其设计意图。因此，相对于预测法定货币的货币供应和铸币率，人们更容易预测加密货币的货币供应量和货币率。

![图 1：美元货币基础与比特币的代币基础之间的比较](img/figure-1.jpg)

*图 1：美元货币基础与流行的
加密货币（比特币）代币基础之间的比较*[^15]

自比特币之后，人们创造了其他各种加密货币。这些加密货币共同组成了一个活跃而充满活力的市场。

降价拍卖
-------------------------

目前，大多数新的加密货币都以传统销售方式提供初始支付。这些销售可能包括奖金、早期买方的定价，以及其他鼓励买方购买所有产品的激励措施。尽管这些激励措施行之有效，但它们并不能保证售出，并且可能导致公共访问不对称。此种模式不适用于以持久性为主要目标的加密货币。Metronome 团队选择使用不同方法来避免这种模式。

Metronome 团队决定采用降价拍卖作为其初始供应拍卖和每日总量批次的模式，这可能提供有趣的机会和更公平的 MET 分配。降价拍卖始于高起始价格。随着拍卖的进行，价格会降低，直到所有单元均售出，或达到预定的底价，或达到拍卖时限而拍卖结束。我们认为市场价格的发现是快速和公平的，因为每个买方在购买时支付自己认为公平的价格。[^16]如果买方认为拍卖价格太高或不公平，可以等价格下降到他们认可的水平再购买，当然，前提是仍有剩余供应。

Metronome 团队选择了这一机制，致力于减轻大型参与者控制 MET 不成比例的供应，提供平等的拍卖机会，并实现更公平的 MET 分配。

Metronome 简介
=====================

Metronome 是一款新型加密货币，最大特点是自治、持久、长期可靠性和最大可迁移性。Metronome 专为拥有机构级的耐久性而设计，它汲取了之前发布的其他加密货币的经验教训，其设计可适应未来的 100 年或更久远。我们相信 Metronome 是一款能够存续上千年的加密货币。

Metronome 的工作原理
===================

![图 2](img/figure-2.jpg)

*图 2：以太坊区块链上的 Metronome 合约之间的流动和相互作用*

**发行**

Metronome 团队的目标之一是提供更公平、更平等的拍卖机会以及 MET 供应。Metronome 的初始供应拍卖和每日总量批次使用降价拍卖 (DPA) 模式。与传统拍卖不同，在降价拍卖中，每个代币的价格从最高价开始拍卖，然后价格慢慢下降，直至所有供应售罄或拍卖结束。Metronome 使用 DPA 旨在建立
透明可预测的定价。[^17]

初始供应拍卖的起拍价为每个 MET 代币等于 2 个 ETH。只要拍卖开放并且仍有 MET 可供购买，价格将每 60 秒钟下降 0.0001984320568 ETH，价格下限为 0.0000033 ETH。

买方实时购买 Metronome 加密货币，并在购买后几乎立即取得其 Metronome。初始供应拍卖期间购买的 Metronome 在初始供应拍卖结束之前不可转让，而在每日总量批次期间购买的 Metronome 在取得后可立即转让。

Metronome 团队认为，以这种方式拍卖使买方有机会以他们认为合理的价格买到 MET，当然，前提是降到该价格时仍有可供购买的 MET。相对于纯荷兰式“每个人都可获得最终价格”拍卖，降价拍卖还会提供更为准确的市场价格发现。原因很简单，因为如果买方愿意高于该价格来支付，说明最终价格本质上被低估了。

这种方法还可以减少大型参与者在拍卖中吸收大量 MET 的机会，因为购买大量不成比例的 MET 的成本可能高于新产生的市场价格。纯荷兰式拍卖仍会以不成比例的价格将 MET 分销给早期买方。

尽管许多供应购买方案是可接受的，但值得强调的是：涓涓细流随后却是汹涌急流。在这种情况下，买方以较高的价格购买少量供应。一旦定价低于某个阈值，剩余的供应可能会被迅速消耗。

**阶段 1：初始供应拍卖**

- 初始代币供应为 1 千万个代币。

- 20% 的初始代币供应由创始人持有。

   - 根据特殊 TokenLocker 合约铸币（见 API 部分）

      - 在初始供应拍卖结束时，25% 可供创始人使用。

      - 剩余的 75% 以等量分 12 个月获得

      - 只有 Metronome 创始人才能撤销他们的 TokenLocker 合约，并且只能在上述特定时间撤销

- 降价拍卖 8 百万个代币（即 1 千万个 MET 的初始代币供应总数减去创始人持有的 20% 代币供应）。

- 初始供应拍卖至多持续 7 天。

- 初始供应拍卖价格定为每个 MET 等于 2 个 ETH，价格下限为 0.0000033 ETH。

- 在初始供应拍卖中，MET 拍卖价格每 60 秒钟就直线下降 0.0001984320568 ETH。

- 拍卖持续进行，直至 8 百万个代币存货售罄或拍卖在 7 整天（10080 分钟）后结束。

- 初始拍卖所得收益的 100% 纳入收益合约中。

**阶段 2：操作货币**

- 在原拍卖结束后，新代币每 24 小时永远按以下两个速率中较大者添加到每日总量批次中：(i) 每天 2880 个 MET 代币，或 (ii) 相当于每年当时未清偿代币供应 2.0000% 的年产率。

- 每 24 小时发起一次拍卖，每次拍卖持续时间不超过 24 小时（为避免拍卖重叠）。

   - 在每日总量批次中，所有代币的降价拍卖从最高价开始，最高价为前一次拍卖收盘价（*例如*，如果拍卖售罄，即为售出的最后一个代币的价格，或者拍卖暂停时的价格）的两倍。

   - 如果在给定的每日总量批次中 Metronome 的售出量为零 (0)，则次日的每日总量批次价格将从每日总量批次中售出的最后一个 Metronome *价格的 1/100 开始拍卖*。

- 每 60 秒钟，拍卖价格就降到原来价格的 99%。

- 拍卖持续进行，直至 (i) 每日总量批次存货全部售罄，或 (ii) 24 小时的拍卖结束，以上述两者中较早者为准。
   - 如果每日总量批次存货没有售罄，剩余 MET 将计入次日的每日总量批次中。

- 每日总量批次的明确价格下限为 1 Wei。

- 每日总量批次所得收益的 100% 转移给收益合约。

- 每隔 24 小时，收益合约总累计余额的 0.25% 就转移给自治转换合约（如下所述），以便 MET 所有者可以出售其 MET。

跨区块链可迁移性
----------------------------

![图 3](img/figure-3.jpg)

*图 3：跨区块链可迁移性演示*

Metronome 独有的特点之一就是跨区块链可迁移性，它允许用户出于任何原因将 MET 从一个区块链移动到另一个区块链。如果用户决定移动自己的 MET，用户必须首先向将接收 MET 的目标区块链做出承诺。用户再从源区块链 A 上的代币供应中删除其 MET 并收到“退出证明”二叉树[^18]收据。然后，用户将此收据提供给目标区块链 B 上的 Metronome 合约。

在这种情况下，区块链 A 上的 MET 代币供应减少，区块链 B 上的代币供应通过此导出/导入过程增加。自治的每日总量批次在区块链 A 和区块链 B 上按比例调整，以反映区块链 A 和 B 中 MET 的新分配。例如，如果区块链 A 和区块链 B 上各存在所有 MET 中的 50%，那么 A 链和 B 链上的每日拍卖都应该是每天 1440 个代币。

导出/导入系统
----------------------------

Metronome 基于其他区块链而构建，这样有助于巩固其自治性质和提高持续存在能力。由于缺乏链条持久性，保持像全球供应这样的常量比使用单区块链加密货币来保持该常量更棘手。因此，Metronome 的导入和导出功能最初分三个阶段推出。随着区块链技术的持续发展进步，其他阶段可能会进一步分散和改善 Metronome 生态系统。

在高层次上，Metronome 可迁移性的组成部分有：

**导出** 所有者可以通过调用导出函数将 MET 从一个区块链上移动到另一个区块链上。这一函数接受用户的 MET，在本地区块链上将它销毁，并以二叉树收据的形式向用户提供一个 ExportReceipt。所有者将以 MET 形式支付一笔小额费用，这笔费用由验证者索取。此收据可用于在目标区块链上认领 MET - 从而有效地将所有者的 MET 从源区块链上移动到目标区块链上。

**导入** 任何用户都可以将 ExportReceipt 提供给预定的目标 Metronome 合约。他们调用 importMET 并提供 ExportReceipt。处理完毕后，目标区块链将 MET 转移给原始接受者。完成 Metronome 导入的用户将在 MET 中获得上述费用用于其认证。

然而，由于 Metronome 支持多区块链，真实来源可能存在于这些区块链中的任何一个上。因此，需要在导入和导出中进行验证。

**验证** 在导入和导出过程中，验证者需要：

证明在硬分叉的情况下哪些区块链是有效的

提供额外信息（如事件证明）以验证特定的导入。

Metonome 的导入/导出基础设施将分三个阶段推出。Metronome 将与第一版一起发行，未来的升级将加入现存的 Metronome 合约。

从概念上讲，验证者在 Metronome 生态系统中的作用类似于其他加密货币中的“矿工”。他们验证并证实 Metronome 的分散真实来源。导出者将在 MET 中向验证者支付可选费用。

验证阶段的系统设计（如下所述）旨在保证：

Metronome 的全球供应量从不超过每日 10,000,000 + 2880（或每年当时未清偿供应的 2%，以较大者为准）。

验证者不能审查个人交易。

避免验证者间产生分歧（见下文）。

其他区块链上的 Metronome 合约可以探测出分歧并“标记”不安全的区块链，最终将其隔离直至它们解决所标识的问题。

验证阶段
----------------------------

阶段 1：验证者通过 ExportReceipt 的散列检查并验证每张导出收据。当足够数量的验证者认定给定的散列有效时，任何人都可以通过验证收据完成 Metronome 的导入。

阶段 2：验证者保存所有导出收据的历史清单，创建收据散列的二叉树，并验证那些树的二叉树根。然后导入者向验证者和用户提供导入证明。导入证明包括二叉树收据和成对的证明事件根源的散列。

阶段 3：验证者验证 Metronome 所在的每个区块链的散列。导入者提供以下证明：

- 通过二叉树路径证明导出事件位于导出链上的某个区块头中。

- 证明区块事件与经过验证的链散列相对应。

不合格参与者的保证和安全措施
----------------------------

由于具有可信赖参与者的阶段 1 验证模型证明了自身，所以社区和团队将继续迭代验证机制，从而使其更加分散。目前，最理想的去中心化水平可能在阶段 3 之后才能达到。验证模型中更大的权力去中心化会以多种方式增加安全性，但仍存在参与者因“非理性”原因而行为不当的可能性。为了解决这个问题，当面对链对链攻击、Metronome 其他分支的故障以及各种其他欺诈类型或错误类型的问题时，系统架构必须具有迅速恢复的能力。
该系统仍在制定中，但广义而言，我们将使用来自更好的权益证明系统的核心概念，结合一些工作量证明概念。Metronome 计划对不合格的参与者“软硬兼施”。Metronome 的基本规则是（并将永远是）：供应量是固定的，用户知道 Metronome 体系的哪些部分是安全的，并且能够将其 MET 导出到安全的地方。

分布式、自愿的共识治理
-------------------------------------------

这种治理模式基于 MET 持有者社区的自愿共识，能够将 Metronome 从其创始人发起的最初“开端”链导出，并导入到其创始人或其他方面发布的后续升级。该功能为两个不可变的合约同时提供了机会，也提供了公平的分配机制来随着市场的成熟而升级这些合约。

例如，如果市场需求量大大超过供应，并且起初 MET 的真实价格上涨超出商家的实际价格，则有些人可能会同意在相同或不同的区块链中，通过将他们控制的资金导出新的分支以新的 MET 合约分散 MET 供应。这些动态有可能消除代币供应曲线中先验设计所带来的风险，因为新的不可变的 MET 合约可以升级代币供应曲线以获得更大的商业用途。

同样，如果市场供应量开始超过需求量并持续一段时间，而且价格下跌，那么不同 MET 分支的持有人可能会同意从多个导出源“合并”到单一输入目的地。这种自愿的共识机制可减少 MET 的总经济活跃供应，从而在需求量减少、价格保持稳定的情况下，使代币供应减少。

至于分支和新链条的移动如何影响 MET 代币供应曲线和发行，在 Metronome 社区中尚无定论。我们诚邀您参与定义、实施、分散和合并您自己的新 MET 目标合约，将 MET 导入新合约，并查看会发生什么情况。

迄今为止的加密货币市场概述
=====================================

为更好地理解 Metronome 对加密货币世界的适应性，我们需要从更高的角度在整体布局上进行讨论。

整体布局
-------------

我们来看几种有名的加密货币，考察其代币供应定位、发行计划以及该计划抗经济恢复力和经济不稳定性的能力。

![图 4](img/figure-4.jpg)

*图 4：目前流行的加密货币铸造，注：ETH 是一种预测*[^19]

比特币（“Bitcoin”或“BTC”）出现于 2009 年 1 月 5 日，大众可以公平地参与该货币生态系统以及进行货币挖掘。[^20]每一个区块出现都会有新的货币供应。每 2016 个区块内，各区块生成时间间隔目标值为 10 分钟。货币供应量为每个区块 50 个比特币，每四年减少一半。

比特币社区精神高度重视比特币 2100 万货币供应限制的不变性，以及发行计划的不变性。一旦达到这一限制，新的比特币挖掘就会停止，交易费用就成为推动矿工进行比特币挖掘的因素。比特币社区内部普遍存在争议，即当货币发行量下降到极低的水平时，交易费用是否足以让比特币获得资金和安全保障。[^21] [^22] 如果比特币今天重新开始，它当前的绝对通缩性质是否会被持久的温和通胀特征所取代，从而刺激矿工为该网络提供无限期的安全保障呢？很有可能。人们期望低水平的通货膨胀，因为它不鼓励囤积资源、*鼓励*投资，就加密货币而言，还会在货币挖掘过程中持续为区块链提供安全保障。[^23]

![图 5](img/figure-5.jpg)

*图 5：比特币和 Metronome 的铸造和流通供应比较*[^24]

今天的用户依赖发行计划的可预测性和不变性。可预测性让市场用户有能力对未来数年甚至数十年进行规划。不变性确保了货币供应不受人类的突发奇想和精神脆弱的影响。然而，比特币社区中有各种各样的团体对影响网络治理感兴趣，使社区出现了争议性分支、不确定性和见解。

莱特币（“Litecoin”或“LTC”）是仿照比特币形成的。[^25] 区块生成时间间隔为 2.5 分钟。货币供应量为每个区块 50 个莱特币，每四年减少一半。从货币发行的角度来看，莱特币基本上是比特币的复制品：发行计划在社区内大多数人来看是不变的。和比特币一样，其新货币发行量会随时间递减。莱特币的管理和比特币类似，但前者对货币生态系统中的明星人物会给予一些习惯性尊重。

大零币（“Zcash”或“ZEC”）也和上述货币类似。工作量证明挖掘对所有人开放。区块生成时间间隔为 2.5 分钟。货币供应量为每个区块 12.5 个大零币，每四年减少一半。特别的是，前 2 万个区块的大零币释放速率相对缓慢，之后才逐渐提高到 12.5 个大零币的释放速率。大零币的开发团队和支持协议开发团队不会一次性将挖掘的货币补偿给矿工，而是会对所有新生成的区块收取代币挖掘量的 10% 作为创始人报酬，直至发行四年后代币供应第一次减半才停止收取。这之后，挖掘出的代币将全部归矿工所有。[^26]大零币基金会旨在成为其货币生态系统自愿治理的天然中心。[^27]

![图 6](img/figure-6.jpg)

*图 6：ZEC 和 MET 创始人保留权益与
流通供应之间的比较*[^28]

以太坊（“Ethereum”或“ETH”）预售筹集了超过 6 千万个以太币，这些都是在开端区块上预挖掘获得的。[^29] [^30] 每生成一个新的区块会供应 5 个以太币。新的货币供应 T+1Y 增长了 19.8%，T+2Y 增长了 21.2%，T+3Y 增长了 17.4%。此后货币增长量逐渐下跌。广为流行的观点是，以太坊货币发行计划不断变化，会随着系统的发展进行改变。[^31]以太坊计划变更其权益证明，这可能会使其发行也有所改变。[^32]因此以太币的发行是可变的，目的是保证其恢复力和可持续性。尽管任何改变都需要货币社区和矿工的支持，但整个社区通常对小部分创始团队非常尊重和信赖。

瑞波币（“Ripple”或“XRP”）的对外供应总数为 380 亿个瑞波币。[^33]其管理公司 Ripple Inc. 还额外拥有 610 亿个瑞波币，其中 550 亿个瑞波币由第三方托管。[^34]瑞波币实行集中管理，Ripple, Inc. 控制着该加密货币生态系统的很大部分。Ripple Inc. 直接管理市场上瑞波币的发行，因此瑞波币发行计划高度可变。Ripple Inc. 保留了不成比例的管理权力。

Metronome 从这些数字货币中吸取了教训，形成一种专为拥有机构级耐久性而设计的加密货币，以发行、治理和可靠性作为其体系结构的主要原则。这种货币具备完全自治性，创始人无法对其施加不正当影响从而违背自我治理的设计目标。Metronome 具备可预测性，以可预测的速率铸造新的 MET，使其保持稳定。用户还可以任何其认为适当的理由在区块链之间转移货币，使其具有可迁移性。

|  | BTC[^35] | LTC[^36] | ETH[^37] | XRP[^38] | ZEC[^39] | MET |
|--|--|--|--|--|--|--|
| **可靠性** | BTC 以其争议性分支和通缩特性而闻名。货币供应和发行稳定，但是有一定限度。| 与 BTC 一样，LTC 的发行和供应受到严格限制，这可能威胁到区块链稳定性。| ETH 的发行和供应模式不断变化。它在过去已经出现过分支。| XRP 的供应稳定，完全由 Ripple Inc. 管理。| 与 BTC 类似，ZEC 受到严格限制，这可能使未来区块链的安全性受到质疑。| **MET 的发行和供应将严格遵循合约，始终可预测。其供应或发行不存在不确定性。** |
| **自治** | BTC 具备自我治理性，但有许多团体想要施加不正当的影响。| LTC 具备自我治理性，但社区对明星人物持有习惯性尊重。| 对 ETH 的改变需要社区的支持，但更依赖于一个小团队。| XRP 不具备自我治理性。Ripple Inc. 保留管理 XRP 的唯一权力。| Zcash 基金会是自愿治理的天然中心。| **MET 通过自治合约实现完全的自我治理。** |
| **可迁移性** | 否 | 否 | 否 | 否 | 否 | **是** |
| **不变性** | 强 | 强 |可变；会随着 PoS 而改变 | 弱 | 强 | **强** |
| **发行模式** | 每 10 分钟 50 个 BTC。每四年减少一半。| 每 2.5 分钟 50 个 LTC。每四年减少一半。| 每 15 秒 5 个 ETH。| Ripple Inc. 发行过一次。| 每 2.5 分钟 12.5 个。每四年减少一半。| **MET 日拍卖量为（以如下两者中较高者为准）：(i) 每天 2880 个 MET，或 (ii) 相当于每年当时未清偿代币供应 2.0000% 的年产率** |
| **供应限制** | 2100 万 | 8400 万 | 未知 | 1000 亿 | 2100 万 | **参见上述发行模式** |
| **结算时间** | 10 分钟 | 2.5 分钟 | 15 秒 | 5 秒 | 2.5 分钟 | 15 秒 |
| **批量支付特征** | 是 | 是 | 否 | 否 | 是 | **是** |
| **认购特征** | 否 | 否 | 否 | 否 | 否 | **是** |

*表 1：当今加密货币之间的重要属性
比较*

Metronome 合约和技术层面
=========================================

四个自治智能合约构成了 Metronome。一般流程为：

1. 第一份合约是 MET 代币和分类账，与区块链直接进行交互。它支持用户进行点对点交易结算，并用作分布式财富存储。它采用大家熟知的具备定制功能的 ERC20 代币标准，具有更高的安全性和转移性。

2. 代币合约之后是拍卖合约。用户通过拍卖合约购买 MET。当用户通过拍卖合约购买时，合约为该用户铸造 MET。

3. 之后拍卖合约会把收益发送给第三份合约——收益合约。初始供应拍卖的每个每日总量批次所得收益的 100% 都将从拍卖合约转移给收益合约。

4. 每隔 24 小时，收益合约将其 0.25% 的收益发送给第四份合约——自治转换合约，为其提供可用的 ETH。当用户向自治转换合约发送 ETH 或 MET 时，合约按各自规定的费率退回 MET 或 ETH。由于自治转换合约中的代币比例决定了它们的相对价值，我们预计套利行为会使定价大致准确。如果合约拥有的 MET（或 ETH）太少，那么与对应合约相比，其价格会相对高昂。如果用户认为自己的 MET（或 ETH）不值那么多，那么该用户会用自己的代币换取其他代币。这样可以平衡合约收益，消除相对价格不平衡。

Metronome 收益和自治转换合约
=====================================================

所有拍卖的一切收益都保留在 Metronome 生态系统中，意图为 Metronome 及其用户构建持久的生态系统。通过确保拍卖中的所有收益保持在合约链中——并且不受任何群体的控制，我们相信 Metronome 可以保持更长和更自治的持久性。

此流程以拍卖合约为起点，合约购买方在拍卖中购买 MET 时与此合约进行交互。然后，收益合约取得拍卖合约的收益，并将一部分导出给自治转换合约，为自治转换合约提供 ETH 供应以进行购买和销售。MET 将在自治转换合约中进行初始化。

在初始供应拍卖和每个后续的每日总量批次中，所得收益的 100% 将转移给收益合约。没有收益分配给 Metronome 创始人。收益合约每天将其累计收益总额的 0.25% 转至自治转换合约。相比直接在自治转换合约中结算收入，我们预计这可能使每日拍卖量的差异较为平滑。

当向自治转换合约出售 ETH 时，合约中特定数量的 ETH 可获得的 MET 数量会增加。这时如果有人出售 MET 并购买 ETH，他们将获得更多的 ETH，如果有人想使用自治转换合约购买 MET，必须支付更多的 ETH。

如果自治转换合约中的 ETH 日销售量将 MET 的价值提高到高于市场可支持的水平，我们相信套利行为将捕获超额 ETH。但是，考虑到 Metronome 的可预测性是以数十年的时间尺度来衡量的，我们预计市场将在自治转换合约可用的 ETH 流量中进行预测和定价。

![图 7](img/figure-7.jpg)

*图 7：与自治转换合约及其后端进程进行交互的用户体验*

**经济预测**

虽然自治转换合约试图接近市场确定的价格，但拍卖合约每天都有固定的定价计划。所以：

- 当拍卖的代币价格高于自治转换合约的代币时，预计买方不太可能从拍卖中购买代币。买方从自治转换合约中购买更便宜的代币显然更划算。

- 当拍卖的代币价格低于自治转换合约的代币时，任何人都可以通过在拍卖中购买代币并将其出售给自治转换合约以获得套利利润。通过套利可以消除自治转换合约中 ETH 存在的不平衡。但是，由于每个人都希望这样做，因此预计拍卖会在价格出现明显差异之前售罄。

总之，预计拍卖中的买方会试图以非常接近自治转换合约当前价的价格在拍卖中购买代币，每个交易日中较晚加入的买方能够从较早买方那里获利，本质上补偿了他们在拍卖中无法购得的风险。

每日总量批次一旦给出，向自治转换合约出售可以满足超额需求，同时可能会提高代币价格。我们预计每次拍卖都会售罄，因为价格最终会下降到低于市场价格。

**数学例子**

当用户与自治转换合约进行交易时，总会存在价格滑点，因为用户正在改变代币供应之间的比例。公式可以确定所有价格，例如不管用户进行大量的小额购买还是一次性大额购买，结果都一样。[^40]

有两个公式：一个用于计算用户获取 MET 或 ETH 的智能代币数量，另一个用于确定用户获取智能代币的 MET 或 ETH 数量。智能代币永远不会向用户公开。

建立准确有效的“初等函数”是一项重大的工程任务。因为以太坊只有 256 位整数，所以新的实施是必要的。

通过将自治转换合约限制为两个加密货币——MET 和 ETH（储备率为 0.5），数学推导得以简化并且只需要一个平方根，这很容易实施并且可以合理有效运行。

数学例子如下：

*R* = 储备代币余额

*S* = 智能代币供应

*F* = 恒定储备率

*T* = 交换储备代币 E 取得的智能代币

*E* = 交换智能代币 T 取得的储备代币

原来的公式是：[^41]

*T* = *S*((1 + $\frac{E}{R}$)${{}^{}}^{F} - 1$)

*E* = *R*(1 - (1 - $\frac{T}{S}$)${}^{\frac{1}{F}}$)

在我们的例子中，因为 F 被设置为 0.5，该公式使用了定点乘法、除法和平方根：

*T* = *S*($$) - 1)

*E* = *R*(1 - (1 - $\frac{T}{S}$)${}^{2}$)

**一个成功的例子**

假设自治转换合约有 1000 个 ETH 和 2000 个 MET，并且有 10000 个智能代币。自治转换合约的 MET 价格为 0.50 ETH。某用户认为数量偏多，希望用 100 个 MET 交换 ETH。在当前名义价格下，他会获得 50 个 ETH，但由于价格下滑，用户实际不会得到这么多。

**第一步**：用 100 个 MET 交换智能代币。

T?=?S?(v1+ E/R )-1)

T? = 10000( v1 + 100/2000 ) - 1) = 10000( v1.05 - 1) = 10000(1.0247 - 1) = 10000(0.0247) = 247

用户取得 247 个新铸造智能代币。智能代币的供应总数现在为 10247。自治转换合约中 MET 的供应总数现在为 2100。

**第二步**：将 247 个智能代币转换为 ETH，由合约自动完成，用户永远不会接触到智能代币。

假设 1000 个 ETH 是公式中的储备供应：

*E* = *R*(1 - (1 - $\frac{T}{S}$)${}^{2}$)

*E* = 1000(1 - (1 - $\frac{247}{10247}$)${}^{2}$) = 1000(1 - (1 - 0.0241)${}^{2}$) = 1000(1 - .976${}^{2}$) = 1000(1 - 0.953) = 1000(0.047) = 47

用户以 100 个 MET 取得 47 个 ETH。

该合约现在包含 953 个 ETH 和 2100 个 MET，或者说每个 MET 对应 0.45 个 ETH。通过出售一些 MET，用户使自治转换合约中 MET 的价格相对于 ETH 降低了。用户大约以初始价格和最终价格的中间价格取得 ETH。

这 247 个智能代币在交易时会被销毁，从而将智能代币供应降低到 10000。

**交易订单减少**

用户可以预测自己的交易结果，前提是在该用户交易之前没有其他交易。这一点无法保证；事实上，其他参与方可以看到用户的交易正在进行，并发布自己的交易订单。矿工可以非常有效地做到这一点。

为了减少交易订单，我们要求用户指定最低回报。如果用户的交易回报低于此值，交易将会撤销；该用户仅需支付一小笔交易费以支付执行交易的计算成本。

代币供应经济学
======================

理论
------

- 供应的可预测性使市场参与者能够准确地测量未来 12 个月、5 年、50 年内的供应量

- 定价通过降价拍卖决定

**供应**

- 初始供应：1 千万个代币，通过降价拍卖

- 初始供应后的供应量：年供应量为以下两者中的较大者：(i) 每天 2880 个 MET 代币，或 (ii) 每年当时未清偿代币供应的 2.0000%

- 拍卖几乎实时结算
   - 一些经济学家认为，由于每个人都以自己的底价支付，因此可以发现拍卖的最佳价格[^42]

### 供应时间表

| 时间 | 流通 MET 代币 | 铸币率 | 每日铸币量 |
|--|--|--|--|
| T + 1 年 | 11,051,200 | 10.512% | 2,880 |
| T + 2 年 | 12,102,400 | 9.512% | 2,880 |
| T + 3 年 | 13,153,600 | 8.686% | 2,880 |
| T + 5 年 | 15,258,880 | 7.399% | 2,880 |
| T + 10 年 | 20,517,760 | 5.400% | 2,880 |
| T + 50 年 | 63,499,700 | 2.000% | 3,411 |
| T + 70 年 | 94,382,561 | 2.000% | 5,070 |

*表 2：供应时间表*

**API 参考**

Metronome 核心
--------------

### 代币 API

用于查询和转移 MET 代币的代币 API 是常见的 ERC20 代币标准。[^43] Metronome 还利用定制功能使自身符合增强的去中心化资金转移和安全性的最新标准。这些改进还使转移更容易对接收合约调用任何函数，允许数据和价值的转移，这一点是 ERC20 代币标准不能单独完成的。Metronome 很自豪能够使用最先进的技术。

**标准 ERC20**

| const name |  Metronome |
|--|--|
| const symbol | MET  |
| const decimals         |  18  |
| function totalSupply   |  符合 ERC20；参考 ERC20 标准。  |
| function balanceOf     |  符合 ERC20；参考 ERC20 标准。  |
| function transfer      |  符合 ERC20；参考 ERC20 标准。  |
| function transferFrom  |  符合 ERC20；参考 ERC20 标准。  |
| function approve       |  符合 ERC20；参考 ERC20 标准。  |
| function allowance     |  符合 ERC20；参考 ERC20 标准。  |
| event Transfer         |  符合 ERC20；参考 ERC20 标准。  |
| event Approval         |  符合 ERC20；参考 ERC20 标准。  |

**定制代币函数**

<table>
<thead>
<tr class="header">
<th>Function multiTransfer(uint[] bits) </th>
<th>允许在单个交易中进行多次资金转移。位数组中的每个 uint 表示一次资金转移；
最左边的 160 位是地址，右边的 96 位是数额。</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>function setTokenPorter(address _tokenPorter) public onlyOwner returns (bool)</td>
<td>为 TokenPorter 设置合约，负责导出功能，这只能由所有者运行</td>
</tr>
<tr class="even">
<td>function mint(address _to, uint _value) public returns (bool)</td>
<td>只有铸币者和 tokenporter 才允许铸造</td>
</tr>
<tr class="odd">
<td>function destroy(address _from, uint _value) public returns (bool)</td>
<td>只有铸币者和 tokenporter 才允许销毁</td>
</tr>
<tr class="even">
<td>function enableMetTransfers() public returns (bool)</td>
<td>此函数将实现 MET 转移，并且只有在初始拍卖结束后才能成功调用。</td>
</tr>
<tr class="odd">
<td>function export(bytes8 _destChain, address _destMetronomeAddr, address _destRecipAddr, uint _amount, bytes _extraData) public returns (bool)</td>
<td>将 MET 导出到 Metronome 支持的另一个区块链。</td>
</tr>
</tbody>
</table>

**二叉树**

下列函数不适合手动使用，但有人
认为它们可以作为有趣的 UI 功能的基础。

| 函数 setRoot(bytes32 root) | 设置与 msg.sender 关联的二叉树根 |
| ------------------------------------------------------------------- | -------------------------------------------------------- |
| Function rootsMatch(address a, address b) constant returns (bool) | 如果两个地址具有匹配的根，则返回 true。 |
| function getRoot(address addr) public view returns (bytes32) | 获取与该地址关联的二叉树根 |

**预订**

这些函数是唯一 Metronome 功能的一部分：区块链上的预订。用户能够通过预订促进
其他用户和机构之间的关系和定期付款。用户通过授权他们提取每周付款来预订。
然后授权组或个人可以将付款从用户账户转移到他们认为合适的任何账户。用户可以在必要时
取消预订。

这解决了其他加密货币一直面临的问题。对许多流行的加密货币来说，
为基于预订的材料进行支付要么无法接受，要么太过繁琐。Metronome 预订功能可以解决这一问题。

<table>
<tbody>
<tr>
<td>function subscribe(uint _startTime, uint _payPerWeek, address _recipient) public returns (bool)</td>
<td>预订某人，即授权他们提取每周付款 _startTime 是预订开始的时间 _payPerWeek 是每周应付代币，包括小数 _recipient 是可以提取代币的人</td>
<tr class="odd">
<td>function cancelSubscription(address _recipient) public returns (bool)</td>
<td>取消预订 _recipient 是您退订的人</td>
</tr>
<tr class="even">
<td>function getSubscription(address _owner, address _recipient) public constant returns (uint startTime, uint payPerWeek, uint lastWithdrawTime)</td>
<td>取得预订信息 _owner 支付，_recipient 是取得预订的人 返回以下信息，startTime 是预订开始的时间 payPerWeek 是接收者每周可以提取的金额 lastWithdrawTime 是接收者上一次提取时间</td>
</tr>
<tr class="odd">
<td>function subWithdraw(address _owner) public transferable returns (bool)</td>
<td>从向您预订的人那里提款，返回成功
_owner 是您的订户</td>
</tr>
<tr class="even">
<td>function multiSubWithdraw(address[] _owners) public returns (uint)</td>
<td>立即从一群订户（所有者）提取资金。返回成功提取的次数。</td>
</tr>
<tr class="odd">
<td>function multiSubWithdrawFor(address[] _owners, address[] _recipients) public returns (uint)</td>
<td>从给定订户（所有者）提取资金给各自的接收者。返回成功提取的次数。</td>
</tr>
<tr class="even">
<td>event LogSubscription(address indexed subscriber, address indexed subscribesTo)</td>
<td>为新用户预订发出</td>
</tr>
<tr class="odd">
<td>event LogCancelSubscription(address indexed subscriber, address indexed subscribesTo)</td>
<td>当用户取消预订时发出</td>
</tr>
</tbody>
</table>

### 拍卖 API

<table>
<thead>
<tr class="header">
<th>Function () payable</th>
<th>标准回退函数；发送 ETH，立即取得 MET 代币</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>function whatWouldPurchaseDo(uint _wei, uint _timestamp) public constant returns (uint weiPerToken, uint tokens, uint refund)</td>
<td>告诉用户在时间 _timestamp 购买的结果是什么，_wei 是要发送的 ETH 的数量，_timestamp 是预期拍卖的时间戳。weiPerToken 是结果价格，tokens 是将返回的代币数量，refund 是用户将得到的 ETH 退款（如果拍卖在本次购买中售罄）</td>
</tr>
<tr class="even">
<td>function isRunning() public constant returns (bool)</td>
<td> 如果拍卖系统已启动，则为 True</td>
</tr>
<tr class="odd">
<td>function currentTick() public view returns(uint)</td>
<td>调用 whichTick 获取当前块的时间戳</td>
</tr>
<tr class="even">
<td>function currentAuction() public view returns(uint)</td>
<td>调用 whichAuction(currentTick())</td>
</tr>
<tr class="odd">
<td>function whichTick(uint t) public view returns(uint)</td>
<td>返回给定时间戳 t 的拍卖时间点，自开端时间起</td>
</tr>
<tr class="even">
<td>function whichAuction(uint t) public view returns(uint)</td>
<td>返回给定拍卖时间点 t 的拍卖实例</td>
</tr>
<tr class="odd">
<td>function heartbeat() public view returns (bytes8 chain,address auctionAddr,address convertAddr,address tokenAddr,uint minting,uint totalMet,uint proceedsBal,uint currTick, uint currAuction,uint nextAuctionGMT,uint genesisGMT,uint currentAuctionPrice,uint dailyMintable,uint _lastPurchasePrice)</td>
<td>返回当前拍卖的统计数据</td>
</tr>
<tr class="even">
<td>function mintInitialSupply(uint[] _founders, address _token, address _proceeds, address _autonomousConverter) public onlyOwner returns (bool)</td>
<td>在初始部署期间调用，以便为创始人铸造初始供应。此函数仅与所有者有关。</td>
</tr>
<tr class="odd">
<td>function initAuctions(uint _startTime, uint _minimumPrice, uint _startingPrice, uint _timeScale) public onlyOwner returns (bool)</td>
<td>在初始部署期间调用设置拍卖开始时间参数。此函数仅与所有者有关。</td>
</tr>
<tr class="even">
<td>function stopEverything() public onlyOwner</td>
<td>暂停当前拍卖的仅与所有者有关的函数。</td>
</tr>
<tr class="odd">
<td>function isInitialAuctionEnded() public view returns (bool)</td>
<td>如果 7 天已过或者所有代币都在初始拍卖中售罄，则为 True</td>
</tr>
<tr class="even">
<td>function globalMetSupply() public view returns (uint)</td>
<td>截至当前拍卖的可用供应总数</td>
</tr>
<tr class="odd">
<td>function globalDailySupply() public view returns (uint)</td>
<td>当前每日拍卖的可用 MET 代币总数</td>
</tr>
<tr class="even">
<td>function currentPrice() public constant returns (uint weiPerToken)</td>
<td>每日拍卖的当前价格</td>
</tr>
<tr class="odd">
<td>event LogAuctionFundsIn(uint amount)</td>
<td>当拍卖合约取得资金时发出</td>
</tr>
</tbody>
</table>

Metronome 收益合约
---------------------------

### 收益合约 API

| event LogProceedsIn(address indexed from, uint value) | 当收益合约取得资金时发出 |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- |
| event LogClosedAuction(address indexed from, uint value) | 当收益将资金投入到 AutonomousConverter 时发出 |
| function () public payable | 处理收益资金来源 |
| function initProceeds(address \_autonomousConverter, address \_auction) public onlyOwner | 在初始部署期间调用。此函数仅与所有者有关。 |
| function closeAuction() public | 在拍卖结束时向 AutonomousConverter 发送资金 |

Metronome 自治转换合约
---------------------------------------

### 自治转换合约 API

<table>
<thead>
<tr class="header">
<th>function () public payable</th>
<th>处理 AutonomousConverter 资金来源</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>function init(address _reserveToken, address _smartToken, address _proceeds, address _auctions) public payable</td>
<td> 在初始部署期间调用。此函数仅与所有者有关。</td>
</tr>
<tr class="even">
<td>function getMetBalance() public view returns (uint)</td>
<td>在合约内显示 MET 余额</td>
</tr>
<tr class="odd">
<td>function getEthBalance() public view returns (uint)</td>
<td> 在合约内显示 ETH 余额</td>
</tr>
<tr class="even">
<td>function convertEthToMet(uint _mintReturn) public payable returns (uint returnedMet)</td>
<td> 将 ETH 转换成 MET。如果返回的 MET 小于 minReturn，则丢弃。返回 
MET 的数量。</td>
</tr>
<tr class="odd">
<td>function convertMetToEth(uint _amount, uint _mintReturn) public returns (uint returnedEth)</td>
<td> 将 MET 转换成 ETH。如果返回的 ETH
 小于 minReturn，则丢弃。返回 ETH 的数量。调用者首先需要批准 AC 进行
转移。</td>
</tr>
<tr class="even">
<td>function getMetForEthResult(uint _depositAmount) public view returns (uint256)</td>
<td>返回用户将由
给定的 ETH 金额得到多少 MET。</td>
</tr>
<tr class="odd">
<td>function getEthForMetResult(uint _depositAmount) public view returns (uint256)</td>
<td> 返回用户将由
给定的 MET 金额得到多少</td>
</tr>
<tr class="even">
<td>event LogFundsIn(address indexed from, uint value)</td>
<td>当 AutonomousConvert 取得资金时发出</td>
</tr>
<tr class="odd">
<td>event ConvertEthToMet(address indexed from, uint eth, uint met)</td>
<td>当发生从 ETH 到 MET 的转换时发出。</td>
</tr>
<tr class="even">
<td>event ConvertMetToEth(address indexed from, uint eth, uint met)</td>
<td>当发生从 MET 到 ETH 的转换时发出。</td>
</tr>
</tbody>
</table>

TokenLocker
-----------

### TokenLocker API

| event Withdrawn(address indexed who, uint amount) | 对所有提取发出 |
| -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| event Deposited(address indexed who, uint amount) | 对所有存款发出 |
| function lockTokenLocker() public onlyAuction | 锁定 tokenLocker。调用此函数将导致 tokenLocker 的 postLock 阶段。不允许再存款。在此阶段允许提取代币。此函数仅与拍卖有关。 |
| function deposit (address beneficiary, uint amount) public onlyAuction preLock | 将资金存入存储器。仅允许在 preLock 阶段进行存款。 |
| function withdraw() public onlyOwner postLock | 资金提取只能在 postLock 阶段进行。此函数仅与所有者有关。 |

TokenPorter
-----------

### TokenPorter API

| event ExportReceiptLog(bytes8 destinationChain, address indexed destinationMetronomeAddr, address indexed destinationRecipientAddr, uint amountToBurn, bytes extraData, uint currentTick, uint indexed burnSequence, bytes32 currentBurnHash, bytes32 prevBurnHash, uint dailyMintable, uint\[\] supplyOnAllChains, uint genesisTime) | 在导出请求期间发出 |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| function addDestinationChain(bytes8 \_chainName, address \_contractAddress) public onlyOwner returns (bool) | 添加链作为认可链用于 metronome 导出。此函数仅与所有者有关。 |
| function removeDestinationChain(bytes8 \_chainName) public onlyOwner returns (bool) | 从认可链中移除链以用于 metronome 导出。此函数仅与所有者有关。 |
| function claimReceivables(address\[\] recipients) public returns (uint) | 此函数的调用方是正在执行 metronome 导入以记录目标合约中 metronome 铸造的目标合约。 |
| function export(bytes8 \_destChain, address \_destMetronomeAddr, address \_destRecipAddr, uint \_amount, bytes \_extraData) public returns (bool) | 导出用户账户以导入另一个区块链 |

合约条款术语表
==========================

- **自治转换合约** 智能合约，允许人们用 ETH 交换 MET，或者将 ETH 转换成 MET。

- **自治收益供应商** Metronome 收益合约与自治转换合约。

- **常量** 包含一些常用常量，如 DECIMALS。

- **每日总量批次** 导致代币生态系统每天都会增加新铸造 MET 的降价拍卖。

- **EVM** 代表以太坊虚拟机。[^44]

- **定点\_数学** 实施定点运算，包括加、减、乘、除、平方、平方根，包括溢出保护。对于二元函数，它会假定两个输入值具有相同的小数位数。

- **公式** 使用定点数学函数运算核心 Bancor 公式。公式具有无状态性，所有变量都只能作为参数。

- **Metronome** 主要拍卖合约。

- **迁移系统** Truffle 迁移能力的一部分。

- **储备代币** 实施 MET。赋予自治转换合约转移代币的权利（响应交易事件）。

- **收益合约** 接受来自 Metronome 的 ETH，每 24 小时将其余额的 0.25% 转让给自治转换合约。

- **智能代币** 自治转换合约发行的代币在通过其合约进行 MET 和 ETH 转换（反之亦然）时充当中介。该过程自发进行，不会向用户公开。

- **代币** 买方购买的 MET 代币。

附录 A
==========

确认和免责声明

购买、使用和/或使用 METRONOME 代币，即表示您明确确认并承担以下风险。

1. **[买方确认]**。作为 Metronome 代币（以下简称“MET”）的买方（以下简称“买方”或“您”），您确认以下几点：

   a.  MET 是[not]作为证券或
其他任何形式的投资产品构建或销售的。MET 尚未按照
美国证券交易委员会 1933 年修订的
《证券法》或
任何国家/地区证券法
或任何其他管辖区的任何类似法律注册，也不适用于
这些法律规定的豁免。因此，用户手册中的信息
不能作为
投资决策的根据，也不构成任何
具体建议。MET 的使用、销售或
处置受用户
手册中的规定的限制。购买 MET 即表示买方
遵守用户手册的所有要求以及
包括美国联邦、州在内的所有司法管辖权区颁布的所有法律
或当地法律。MET 的创造者明确声明对
直接或间接造成的任何直接或间接损失或
损害不承担任何责任，
包括因下列各项导致的损失或损害：(i) 依赖用户
手册或其他文件中包含的信息，(ii) 此类信息的任何错误、遗漏
或不准确，或 (iii) 此类信息导致的
任何行为；

   b.  本文件尚未登记，
将不会作为新加坡金融管理局的招股说明书登记，且不是
《证券与期货法》(SFA) 中规定的招股说明书
（新加坡第 289 章）（“**SFA**”）。因此，SFA 关于
招股说明书的法定责任
不适用；

   c.  您不会使用 MET 或 Metronome 来创建由美国商品期货交易委员会
监管的产品，包括
期货合约、掉期交易或零售商品
交易。您还确认购买 MET 不用于
任何形式的期权
或掉期交易；

   d.  您了解与
加密代币、代币存储机制（如加密
钱包）和区块链技术相关的技术和业务问题，了解 MET 并
知晓使用、购买
和/或处理 MET 的风险与后果；

   e.  您已获得足够的有关 MET 的信息来
做出明智购买 MET 的决定，并且不依赖
用户手册中提供的任何信息
来做出购买 MET 的决定；

   f.  您知道 MET 只授予在
用户手册中设想的 MET 的权利。MET 不授予任何形式的
其他权利，包括但不限于实体所有权、
分配权、赎回权、清算权、专利权
（包括任何形式的知识产权）、财务
或法律权限；

   g.  您只是按照用户手册中设想的 MET 
购买 MET，并知晓
与 MET 相关的商业风险。您不会出于其他目的
购买 MET，包括但不限于任何
投资、投机或财务目的；

   h.  您购买 MET 的行为符合您所在司法管辖区的
适用法律和法规，包括但不限于 
(i) 购买 MET 的合法能力和
任何要求或限制，(ii) 适用于
此类购买的任何外汇或监管限制，以及 (iii) 任何
可能需要获得的政府或其他部门的批准；

   i.  您全权承担您购买或使用 MET 
产生的任何适税义务；

   j.  如果您代表实体购买 MET，您有权
代表实体
同意这些确认和免责声明；

   k.  您不是 (i) 适用法律、法令、条例、条约或行政法案
禁止接受 MET 交付的地区的
公民或居民，
(ii) 位于受联合国、欧盟、美国或其他主权国家/地区
制裁或禁运的地区的
公民或居民，或 (iii) 美国商务部的被拒人士或实体名单、
美国财政部特别指定的国民或被冻结人员名单、
美国国务院禁止的缔约方名单、
类似的受限制人员条例
或任何其他适用主权国家/地区的名单、
或任何前述或后续规章限制的
任何个人
或受实体雇用或与实体有关的个人。您同意
若您居住的国家/地区或其他情况发生变化，
导致以上确认不再准确，您将
立即停止使用 MET；

   l.  MET 的价值取决于人们是否接受它
作为加密货币使用，
以及它被用于支付商品和服务的程度。需求不足可能使 MET 
难以用于支付货物和服务，这往往会
降低 MET 的价值。同样，如果不采用 MET，
价值通常也会降低。此外，
近期内仍存在对加密货币和代币销售的
重大监管风险，
这可能会大大降低 MET 的价值；

   m.  MET 的价值应主要取决于
使用 MET 作为支付商品和服务的加密货币
的普遍价值；

   n.  MET 作为加密货币，
由于竞争和市场条件影响了总体供需，
MET 的价格会发生波动。这些条件超出了任何特定方
或 MET 持有者的控制范围。MET 
在使用或交换时的价值
可能低于购买时的价格；

   o.  定期、自主、独立发布新的 MET 
旨在稳定 MET 价格，
以实现 Metronome 生态系统服务的内在价值，但
无法保证此类 MET 发布，
并且可能会以任何价格为自己的账户购买和销售 MET；

   p.  出售 MET 并不会限制
 Metronome 参与其他项目、运营其他网络
或发行可能与 MET 竞争的其他代币的权力；

   q.  不承诺
 MET 的未来表现或价值，包括不对内在价值、
继续付款进行任何承诺，
也不保证 MET 将保留任何特定价值；并且

   r.  Metronome 创始人对于如何使用自己的
 MET 销售收益没有任何条件。

2. **[确认某些风险]**。您确认
 MET 存在以下风险，并同意
您明确承担这些风险：

   s.  ***MET 的自治性***。MET 自治运营，
没有任何一方能够影响或控制
 MET 的运营。MET 的自治性可能
会在未来造成风险，包括您在发行 MET 或购买时
无法预见的风险。

   t.  ***由于丢失私钥、
保管错误或买方错误而失去 MET 访问权限的风险。*** 私钥或
私钥组合对于
控制和处理存储在数字钱包或保险库中的 MET 必不可少。因此，丢失
与数字钱包或存储 MET 的保险库相关的必要私钥
将导致该 MET 的丢失。此外，
任何获得此类私钥的第三方，
包括通过访问您使用的托管钱包服务的登录凭据，
都可能会盗用 MET。由您选择取得和存储 MET 的
数字钱包或保险库
所引起的与之相关的任何错误或故障，
包括您自己未能妥善维护或使用此类数字钱包或保险库，
也可能导致 MET 丢失。
此外，如果您没有严格遵守
购买和取得 MET 所规定的程序，例如，
如果您提供了错误地址，则可能会导致 MET 丢失。

   u.  ***与区块链协议相关的风险。*** 任何
故障、分解或放弃 MET 赖以运行的区块链协议
都可能对 MET
 产生重大不利影响。此外，密码学或技术方面的进步
可能会给 MET 带来风险，
因为这会使
支持区块链协议的密码协商机制无效。

   v.  ***挖矿攻击的风险。*** MET 在区块链验证 MET 交易的过程中
容易受到矿工的攻击，
包括但不限于双重支付攻击、
多数挖矿动力攻击、选择性延迟或交易审查
以及自私挖矿攻击。任何成功的攻击
都会给 MET 带来风险，包括但不限于
涉及 MET 交易的精确执行和记录。

   w.  ***黑客攻击和安全弱点的风险。*** 黑客或其他
恶意团体或组织可能尝试以各种方式干扰 
MET，包括但不限于恶意
软件攻击、拒绝服务攻击、基于共识的攻击、
SybIL 攻击、欺骗。此外，由于 MET
 基于开源软件而构建，因此第三方
可能有意或无意地将弱点
引入新 MET 实施的核心基础设施，这
可能会对 MET 产生不利影响。黑客或其他恶意团体
或组织也可能试图访问私钥，
钱包、保险库中的其他访问凭据，
或用于取得和保留 MET 的其他存储机制。

   x.  ***与 MET 市场相关的风险。***如果 MET 的二次交易
由第三方交易所促成，
则此类交易所可能相对较新，且很少受
监管监督或根本不受监督，因此更容易受到欺诈或
操纵。此外，就第三方确实
将外汇交易价值归于 MET（例如，以
数字或法定货币计价）而言，此价值可能极易
波动，并可能减少至零。

   y.  ***无保险的损失风险。***与某些银行账户
或其他金融机构的账户不同，MET 没有保险。
因此，在效用价值损失的情况下，没有
公共保险公司或私人保险为您提供追索权。

   z.  ***与不确定的法规和执法行动
相关的风险。*** 在许多司法管辖区，MET 和分布式分类账技术的监管状况
尚不清楚或未得到解决。对于包括 MET 在内
的这类技术及应用，
很难预测监管机构如何或是否
应用现有法规。同样，很难
预测立法机构或监管机构
如何或是否修改影响分布式分类账技术及其应用（包括 MET）
的法律法规。
监管措施可能以各种方式对 MET 产生不利影响，
包括仅出于说明目的，通过
确定 MET 的购买、销售和交付
构成非法活动，或 MET 是需要就这些手段
进行注册或许可的受管制工具，
或者在购买、销售和交付过程中
涉及的部分或所有各方。

   a.  ***税收带来的风险。*** MET 的税务特征
不确定，可能导致不利的税务后果，
包括预扣税、所得税和税务申报
要求的变化。您必须寻求与 MET 有关的
税务建议。

   b.  ***技术风险***MET 代表了一项尚未得到充分证明的
新兴技术新功能。随着
技术的成熟，新功能可能会极大地改变
MET 的有用性或者使用或销售 MET 的能力。

   c.  ***意外风险。*** 除了本附录所包含的风险之外，
还存在与
购买、持有和使用 MET 相关的其他风险，包括
意外风险。此类风险可能会进一步发生变化
或演变成为本附录提到的
风险组合。

<!-- -->

1. **[免责声明]**。每个 MET 均在“现状”和“现有”的基础上进行销售，不含任何形式的担保，包括但不限于对适销性、特定用途的适用性、所有权或非侵权的暗示保证。

[^1]: <https://medium.com/\@jgarzik/bitcoin-is-being-hot-wired-for-settlement-a5beb1df223a>

[^2]: <https://bitcoin.org/bitcoin.pdf>

[^3]: <https://bitcointalk.org/index.php?topic=47417.0>

[^4]: <https://www.economist.com/blogs/freeexchange/2014/04/money>

[^5]: <https://econjwatch.org/file\_download/139/2007-01-hummel-com.pdf?mimetype=pdf>

[^6]: <https://econjwatch.org/file\_download/139/2007-01-hummel-com.pdf?mimetype=pdf>

[^7]: Tsiang, S.C., Journal of Money, Credit and Banking, I(1969), pp.
266--80 \"A Critical Note on the Optimum Supply of Money\"

[^8]: <https://medium.com/\@MetronomeToken/on-metronome-author-retention-and-contract-behavior-73dad8f16494>

[^9]: <https://medium.com/\@MetronomeToken/proceeds-for-the-community-not-the-authors-d41874d4d41f>

[^10]: <http://onlinelibrary.wiley.com/doi/10.3982/TE502/pdf]](http://onlinelibrary.wiley.com/doi/10.3982/TE502/pdf>

[^11]: <http://markets.businessinsider.com/news/stocks/Etherparty-Pre-sale-Sells-Out-Receives-Over-25MPublic-ICO-sale-launches-Oct-1-1002374859>

[^12]: <https://medium.com/\@MetronomeToken/what-is-a-descending-price-auction-8c0770bb6a71>

[^13]: <https://medium.com/@MetronomeToken/fairness-as-a-first-order-variable-8012a5c22ed1>

[^14]: <https://medium.com/\@MetronomeToken/self-governance-as-a-design-goal-fc06afd61dd5>

[^15]: 来源：coinmarketcap, coinbase, blockchain.info, Federal Reserve Bank of St Louis

[^16]: <http://onlinelibrary.wiley.com/doi/10.3982/TE502/pdf>

[^17]: Mishra, Debasis, and David C. Parkes. "Multi-Item Vickrey-Dutch
Auctions." Games and Economic Behavior, vol. 66, no. 1, 2009, pp.
326--347., doi:10.1016/j.geb.2008.04.007.

[^18]: <https://en.bitcoin.it/wiki/Protocol\_documentation\#Merkle\_Trees>

[^19]: 来源：coinmarketcap.com, coinbase, blockchain.info

[^20]: <https://bitcoin.org/bitcoin.pdf]](https://bitcoin.org/bitcoin.pdf>

[^21]: <https://bitcointalk.org/index.php?topic=108964.0>

[^22]: <http://www.thebitcoin.fr/wp-content/uploads/2014/01/The-Economics-of-Bitcoin-Mining-or-Bitcoin-in-the-Presence-of-Adversaries.pdf>

[^23]: <https://www.brightscope.com/financial-planning/advice/article/8491/Asked-Answered-Zero-Inflation/>

[^24]: 来源：coinmarketcap.com, coinbase, blockchain.info

[^25]: <https://bitcointalk.org/index.php?topic=47417.0>

[^26]: <https://z.cash/blog/founders-reward-transfers.html>

[^27]: <https://z.cash/blog/funding.html>

[^28]: <https://z.cash/blog/founders-reward-transfers.html>

[^29]: <https://github.com/ethereum/wiki/wiki/White-Paper>

[^30]: <https://blog.ethereum.org/2014/08/08/ether-sale-a-statistical-overview>

[^31]: <https://twitter.com/VitalikButerin/status/879675471532654595>

[^32]: <https://github.com/ethereum/wiki/wiki/Proof-of-Stake-FAQ>

[^33]: <https://coinmarketcap.com/currencies/ripple/>

[^34]: <https://ripple.com/insights/ripple-to-place-55-billion-xrp-in-escrow-to-ensure-certainty-into-total-xrp-supply/>

[^35]: <https://bitcoin.org/bitcoin.pdf>

[^36]: <https://bitcointalk.org/index.php?topic=47417.0>

[^37]: <https://github.com/ethereum/wiki/wiki/White-Paper>

[^38]: <https://ripple.com/insights/ripple-to-place-55-billion-xrp-in-escrow-to-ensure-certainty-into-total-xrp-supply/>

[^39]: <http://zerocash-project.org/media/pdf/zerocash-extended-20140518.pdf>

[^40]: <https://drive.google.com/file/d/0B3HPNP-GDn7aRkVaV3dkVl9NS2M/view>

[^41]: <https://www.bancor.network/static/bancor\_protocol\_whitepaper\_en.pdf>

[^42]: <http://onlinelibrary.wiley.com/doi/10.3982/TE502/pdf>

[^43]: <https://theethereum.wiki/w/index.php/ERC20\_Token\_Standard>

[^44]: <http://ethdocs.org/en/latest/introduction/what-is-ethereum.html>

