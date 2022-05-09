# 开源生命周期管理

* 现代化软件开发生命周期管理
  生命周期角度，探讨如何持续构建高安全产品的研发能力

  *  Why：从客户问题、产业现状、企业竞争力三个视角看生命周期面临的挑战，转变对生命周期的意识
  *  What：优选解决优生问题，生命周期解决死的问题。从合同/产品/硬件/软件版本/平台/工具/开源软件各层识别挑战
  *  How：以某产品实际面临问题为实战，探讨如何做生命周期管理，谁来做，怎么做？

## 认识软件版本生命周期所面临的挑战，转换意识

### 发现身边的安全隐患

假如明天产品发布，突然收到100个漏洞单，在这种情境下，你怎么处理？

* 先发布？
* 发布之后怎么解决或者是需不需要解决？
* 客户是否认可？

### 客户需要的是持续、系统的安全

| 产品代码质量问题                                             |   从安全视角重新理解   |
| ------------------------------------------------------------ | :--------------------: |
| 来源可靠                                                     |       用的是真的       |
| 编码安全规范：1.自研2.开源软件整改                           | 所有代码需要代码级安全 |
| 1.片段使用2.老软件3.一个开源软件多版本4.多平台产生多副本5.多平台自身副本 |      扩大了攻击面      |
| 组件生命周期覆盖软件版本生命周期                             |   客户实际想要的是？   |
| 所有公开开源软件漏洞都在代码层面修复                         |   客户实际想要的是？   |
| 现网升级                                                     |   客户实际想要的是？   |

### 产业现状：开源社区既是创新沃土，又易被黑客利用

整个信息行业占80%的代码都使用到了开源软件，一旦发生漏洞，像openssl这种高危漏洞，系统很容易被攻破。所以从开源软件整个安全观来讲，其实是要上升到我们整个产品的安全观来看。这就是为什么开源软件的生命周期管理实际上升到一个维度，其实是产品的生命周期管理的个问题。

* 开源社区是创新沃土，广泛应用于产品
* 开源的漏洞易被黑客利用，漏洞一旦公开必须快速在产品修复

### 企业竞争力与现代软件开发的核心矛盾（1/3）- 分与合的矛盾

问题：把所有的安全问题都解决了，所有的合规的问题也解决了，但会导致花大量的精力、时间和人力去维护、修复这些问题，就没有时间没有人力去做竞争力的问题，怎么解决呢？实际上这就是现代软件开发当中的一个核心的矛盾，这就是一个分与合的一个矛盾。

* 竞争力：分布式交付模式、大平台战略大幅提升产品线质量/效率/竞争力
* 挑战：7层平台嵌套，不同时期立项的平台引入同一款开源软件的当期版本造成最终产品中同一款开源软件版本多
  * 不归一：老平台一直在网使用，导致单产品同时使用一款软件的不同版本
  * 版本老：考虑到稳定性因素，部件年龄老化，采用延长维保覆盖产品生命周期
  * 多副本：基于开源修改，片段代码散落在平台代码中

### 产品竞争力与现代软件开发的核心矛盾（2/3）- 稳定与升级的矛盾

* 竞争力：稳定性可靠性，产品不愿意升级平台，客户不愿意升级产品
* 挑战：升级新版本才能规避漏洞
* 建议：竞争力跟产品安全、产品合规是一个严峻的挑战。例如，某一个公司，要修复一个漏洞，安全部门观察到现在某一个开源软件包含了一个漏洞，请产品去修复这个漏洞，安全响应部门它已经将所有的漏洞包括它的行为都已经归档了。但是产品在过程中是否修复了呢？产品修复肯定是在新版本的软件包里修复的，或者是给一个新版本的补丁。从企业内部来说有可能产品确实是修复了，也打了包了，但是到客户，到我们的销售部门，到了维护团队，整个修复的流程是否真的都做到了？如果没有这样的一个跟踪机制的话，实际上是不清楚的，因为涉及到中间的环节太多了。代码级安全不是说在企业的研发的阶段代码级安全，而是要在客户那里，包括提交的二进制提代码，只要给客户了，所有的程序都要做到代码级安全。假如说有些产品因为某种原因不停迭代，新版本和老版本都在老的硬件上，到时候会不会因为要兼容老的硬件，所以某些软件就不能升级？这种就是一个新的兼容性的一个挑战。

### 产品竞争力与现代软件开发的核心矛盾（3/3）- 长生&不老的矛盾

产品合同约束的时候，可能给客户约束了一个时间非常长的一个合同，可能10年、15年。但是实际上软件的升级维护是有期限的。有些开源软件可能在社区就撑不过四年、五年，到社区说软件停止维护了，再去升级，就不现实了。所以有一个问题，就是产品合同是不是一定要这么长的时维护时间？是否有更灵活的升级或者更新的一个机制？这么多问题，这么多挑战，是否有一些新的看法呢？大家是否认为，为了保障产品的竞争力，安全也好，合规也好，问题的修复也好，是否可以忽略呢？我们需不需要从一个新的安全的角度去理解这个问题？

## 探讨如何持续构建高安全产品的研发能力

### 管生：优选

开软件约束产品的生命周期。前面提到了产品在设计的时候要选择相应的开源软件，一定是按某些规则来进行的优选。比如我们需要通过它是否合法合规，是否有网络安全漏洞，它的兼容性怎么样，社区的活跃度怎么样，从这些维度来去管理它的优选的情况。建议在不同产品去制定相应的规则，使开源软件能够被管控，特别是选用了优选的软件，是要进行独立的管控的。

### 开源软件技术组织和产品线的矩阵管理

成立软件选型专家组织，集中把控软件选型：
在做优选的时候，要有相应的开源软件的一些技术组织，对开源软件来进行管控。比如说对软件的分类，专家对软件进行分类，按照分类，专家评估，评估报告会影响产品引入开源软件的优先级。在产品经理团队、架构师团队里，应该也有相应的专家能对产品做分层的管理，把开源软件的优选管控起来，只有这样形成一个矩阵化的管理，才有相应的保障。

### 管死：退出机制 挑战：层层嵌套带来的配套复杂性

从产品的生命周期开始就包含有很多很多内容，可能涉及硬件开发，也有可能是软件云平台类的软件，应用类的软件，或者是某些驱动，构建工具的软件，这些都需要有生命周期的规划。软件的生命周期一定要包含上层软件的生命周期，也就是说平台软件也好，驱动也好，它的生命周期一定要包含上层应用的生命周期。

### 产品各层级生命周期可维护

制定产品生命周期的时候，一定要注意生命周期可维护。产品硬件，软件它都有生命周期的模型的约束，产品是要不断迭代演进的，如果某一个产品版本一直用下去，肯定会出现网络安全问题的。硬件也是有生命周期的，因为硬件很难去被替换，所以我们在硬件设计的时候要预留相应的空间，使得我们的软件能够进行升级，不能因为硬件而不允许升级，相应的产品的软件平台，工具、芯片、软件，同时能够保证升级，不会被上一层和下一层的软件生命周期所约束。

### 生命周期管理长效机制总体策略

* 对外：完善供应商、企业、客户三个对象的生命周期规则，确保产业链生命周期不脱节
* 对内：完善各对象的配套关系，建立完整的产品树，确保生命周期风险可视 & 可控

### 生命周期优化必须解开两个扣：产品必有死期，合同必有约束

生命周期的管理总结：产品它必有死期，产品无限制的固定的维护下去，一定有死亡或者是退出生命周期的那一天。也就是说软件和硬件要不停的去迭代，只有迭代才能够保证软件当中的安全问题、合规问题能够被解决掉。从这点来说，我们跟客户谈合同的时候，合同也要有一定的约束，不能说这个合同就是无限制，对某一个老的硬件或产品一直维护下去，这是不切实际的，总有一天会有大量的安全问题，产品不可用，带来商业上的一个损损害。从研发的角度来说，要持续的产品和研发能力，保证所有的东西都是可以维护的，也是能够易于被升级的。