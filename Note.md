# 人月神话

## 焦油坑 (The Tar Pit)

- 程序成为编程产品需要增加3倍的工作量，集成到产品系统中还需要3倍的工作量，一共9倍。
- 编程职业的乐趣包括：创建事物、开发对他人有用的东西、组装出预期结果的成就感、持续学习和介质易于驾驭。
- 编程职业的烦恼包括：必须追求完美、目标 资源 信息由他人提供、琐碎的bug、产品可能过时。

## 人月神话 (The Mythical Man-Month)

软件项目缺乏合理的时间进度的原因有：

- 弥漫在程序员中的乐观主义。
- 人数和工作时间往往不可替换。
- 对系统测试时间进度安排不合理。
- Brooks 法则：*向进度落后的项目中增加人手，只会使项目更落后*。

## 外科手术团队 (The Surgical Team)

优秀的程序员比平庸的程序员生产率高得多，软件经理更喜欢少量精干的队伍。对于这样的队伍如何开发大型项目，Mills给出了队伍配置方案：

- 首席程序员，负责定义功能和性能技术说明书，设计程序，编写源代码，测试及书写技术文档，需要极高的天分和大量的经验和知识。
- 副手，首席程序员的后备，经验较少，参与思考、讨论和评估，可以参与代码编写。
- 管理员，控制财务、人员、工作地点安排，专业管理机器，沟通组织中其他管理机构。
- 编辑，对首席程序员的草稿或口述进行分析和重新组织，提供参考信息，维护和监督文档生产。
- 两个秘书，管理员和编辑各一个，负责项目的写作一致和非产品文件。
- 程序职员，负责维护技术记录。
- 工具维护人员，保证所有基本服务的可靠性，构建、维护和升级团队所需工具。
- 测试人员，是首席程序员日常调试设计测试数据的助手，负责计划测试的步骤和为测试搭建测试平台。
- 语言专家，掌握复杂编程语言的人，寻找一种简洁、有效的使用语言的方法来解决复杂、晦涩或者棘手的问题。

对于大型项目可以使用多个这样的队伍，由于协调时只需要协调首席程序员，大大减少了沟通成本。

## 贵族专制、民主政治和系统设计 (Aristocracy, Democracy, and System Design)

- 软件概念上的一致性是为了软件的易用性，易用性的衡量指标是功能和理解复杂程度的比值。
- 获得概念上的一致性，可以通过上一章的人员团队实现，也可以通过对工程进行垂直划分实现
- 创造性活动可以划分为三个独立的阶段：体系结构 (architecture)、设计实现 (implementation)、物理实现 (realization)。
- 获得概念上的一致性没有剥夺实现人员创造的乐趣，反而可以让他们关注于解决具体的问题，获得更好的创造灵感。
- 三个阶段可以同时开始进行，实现不需要等待结构设计结果完全出来才开始准备。

## 画蛇添足 (The Second-System Effect)

结构设计需要联系实现情况，不能过分设计，为了达到这一点，结构设计师需要做到：

- 与开发人员的有效沟通
  - 牢记是开发人员承担创造和发明性的实现责任，所以设计师只能建议，而不能支配。
  - 时刻准备着为所指定的说明建议一种实现的方法，同样准备接受其他任何能达到目标的方法。
  - 对上述建议保持低调和平静。
  - 准备放弃坚持所作的改进建议。
- 自律(尤其是第二个系统)
  - 结构设计师普遍倾向过分设计第二个系统，往往是他第一个系统由于谨慎而舍弃的功能。
  - 结构设计师应该有意识关注这些危险性，自我约束。

## 贯彻执行 (Passing the Word)

为了保持系统中结构师的概念一致性，确保实现人员听从、理解并实现结构师的决策，可以从以下几个方面做出努力：

- 手册
  - 手册是产品的外部规格说明，要描述包括所有界面在内的用户可见一切，避免描述用户看不见的东西。
  - 手册修改的阶段化很重要，应该带有版本信息。
  - 手册说明必须清晰、完整、准确和一致，精确比生动更加重要。
- 形式化定义
  - 形式化定义的优点是精确缺点是不易理解，往往会搭配记叙性文字一起使用。
  - 同时使用两种定义时，必须指定一个作为标准。
  - 实现也可以作为一种定义，比如仿真装置，其缺点是可能过度地规定了外部功能。
- 直接整合
  - 通过规定接口语法强制定义
- 会议和大会
  - 少量问题直接相关人举行频繁地会议，得出迅速的结论。
  - 系统所有人每隔一段较长时间进行大会，对于会议中没有解决的问题以及其他问题进行讨论和决定。
- 多重实现
  - 对于同一定义，给出多种实现，这样当实现与定义不符时，应该去选择实现，而不是去修改定义。
- 电话日志
  - 应鼓励实现人员与结构师直接交流。
  - 结构师应该保存交流日志，并进行整理，并发布给用户和实现人员以帮助理解。
- 产品测试
  - 产品测试小组是用户的代言人，必须严格的测试定义有没有被贯彻执行。

## 为什么巴比伦塔会失败？(Why Did the Tower of Babel Fail?)

巴比伦塔失败的原因是缺乏交流和组织，大型项目中的交流和组织也同样重要。
团队中的交流包括非正式途径、会议和工作手册。

- 项目工作手册
  - 项目工作手册是对项目必须产出的一系列文档进行组织的一种结构。包括目的、外部规格说明、接口说明、技术标准、内部说明和管理备忘录。
  - 项目手册应确保信息能到达所有需要它的人的手中。
  - 可以使用树状索引结构来维护发布列表。
  - 手册的实时更新非常关键，需要持续的文档维护。
  - Parnas 指出，编程人员仅需了解自己负责的部分，其他部分只需要了解接口就好。
- 组织架构
  - 组织的目的是减少不必要交流和合作的数量。
  - 减少交流的方法是人力划分和限定职责范围。
  - 管理结构是树状的，但是交流是网状的。
  - 产品负责人和技术主管有三种关系，同一个人、产品负责人为主、技术主管为主。

## 胸有成竹 (Calling the Shot)

- 软件工程的工作量往往是规模的幂指数，有数据表明指数是1.5
- 每个技术人员的工作时间会浪费在琐碎工作中，如果忽视这一点，往往会造成对进度乐观估计。
- 对于常用的编程语言而言，生产率是固定的。
- 使用适当的高级语言，编程生产率可以提高5倍。

## 削足适履 (Ten Pounds in a Five-Pound Sack)

软件的所需要的空间同样是软件的成本。可以从以下几个角度考虑减小空间成本：

- 规模控制
  - 应该制定总体规模的预算，也应该指定后台存储访问的预算，
  - 指定模块多大的同时，确定模块的功能。
  - 培养开发人员从系统整体出发、面向用户的态度。
- 空间技能
  - 功能换空间，减少功能，或者设计成功能可选。
  - 时间换空间，基础库应该至少有两个版本，速度快的和空间小的。
- 改进数据结构
  - 改进数据结构和算法往往能从战略上改良空间。

## 提纲挈领 (The Documentary Hypothesis)

- 软件项目的文档包括：
  - 目标：定义了待完成的目标、迫切需要的资源、约束和优先级。
  - 产品技术说明：以建议书开始，以用户手册和内部文档结束。速度和空间说明是关键的部分。
  - 进度表。
  - 预算。
  - 工作空间分配。
  - 组织图。
- 正式文档的意义
  - 书面记录决策才能得到清晰、确定的策略。
  - 文档能够作为与其他人的沟通渠道。
  - 文档可以作为数据基础和检查列表

## 未雨绸缪 (Plan to Throw One Away)

- 软件工程常常要抛弃第一次开发的原型，重新开发，因此在计划中就要考虑到后来可能的变化。
- 要为变化计划系统：细致的模块化、可扩展的函数、精确完整的模块间接口设计和完备的文档。可以使用高级语言和自文档技术以减少变更引起的错误。
- 要为变化计划组织架构：高级管理人员与技术人员要有互换性。
- 软件维护：
  - 维护总成本通常是开发成本的40%或更多。
  - 在上一个版本中被发现和修复的bug，在新版本中仍会出现，新版本的新功能会产生新的bug。
  - bug 数随软件安装时间呈U型发展。
  - bug修复总会以(20-50)%的几率引入新的bug。
  - 回归测试是必要的，但是成本很高。
  - 使用消除或者至少指明副作用的程序设计方法，会减少维护成本。
- 软件维护永远是增加系统混乱度的过程，崭新的，基于原有系统的重新设计是完全必要的。

## 干将莫邪 (Sharp Tools)

有很多技术和设备可以显著提高开发效率和质量。

- 目标机器
  - 目标机器是软件服务的对象，程序必须在该机器上进行最后调试。
- 辅助机器和数据服务
  - 仿真装置，在新机器还不完善的时候，需要一个可靠的调试平台。
  - 编译器和汇编平台。
  - 编程工具。
  - 文档系统。运行在可靠平台上的，计算机化的文本编辑系统。
  - 性能仿真装置。尽早开始性能和逻辑仿真。
- 高级语言和交互式编程
  - 高级语言有利于生产率和调试速度。
  - 有数据表明，交互式编程的生产率至少是原来的两倍。

## 整体部分 (The Whole and the Parts)\

如何开发一个可以运行的系统？

- 剔除 bug 的设计
  - 防范 bug 的定义：细致的功能定义、详细的规格说明和规范化的功能描述说明。
  - 测试规格说明：规格说明必须在编写任何代码前交给测试小组，以详细地检查说明地完整性和明确性。
  - 自顶向下的设计。
  - 结构化编程：尽量避免通过 GO TO 不加限制的分支跳转。
- 构建单元测试
  - 使用交互式编程和良好的测试用例。
- 系统集成测试
  - 使用经过调试的构建单元。
  - 搭建充分的测试平台：伪构件，伪文件，辅助程序。
  - 控制变更，必须有人负责控制各个构件单元的变更或者版本之间的替换。系统的拷贝包括：供构件单元测试使用的最终锁定版本，测试版本，安全版本。
  - 一次添加一个构件，并进行回归测试。
  - 阶段化、定期变更。

## 祸起萧墙 (Hatching a Catastrophe)

软件工程进度大幅落后往往是每天一点小落后引起的，为了避免这种情况，可以采取如下措施：

- 进度表中的每个事件应该是具体的、特定的、可度量的事件。
- 随时确定任务中的关键路径，督促开发人员避免自己的工作成为关键路径。
- 老板为了获取真实的进度信息，应该
  - 区别行动信息和状态信息，不对项目经理可以解决的事做出反应，不在检查状态时安排行动。
  - 拥有对项目进行定期评审的机制。
  - 相信基层经理对工作进度的估计，力求得到精确没有偏见的估计。

## 另外一面 (The other face)

软件的文档是将软件的信息传递给程序员和用户的重要手段。

- 需要什么样的文档
  - 对于使用程序的用户，软件文档应当包括：
    - 目的，主要功能是什么？开发程序的原因是什么？
    - 环境，程序运行在什么样的机器、硬件配置和操作系统上？
    - 范围，输入的有效范围是什么？允许显示的合法范围是什么？
    - 实现功能和使用的算法。
    - 输入输出格式，必须是确切和完整的。
    - 操作指令，包括控制台及输出内容中正常和异常结束的行为。
    - 选项，用户的功能选项有哪些？如何在选项之间进行挑选？
    - 运行时间，在指定的配置下，解决特定规模问题所需要的时间？
    - 精度和校验，期望结果的精确程度？如何进行精度的检测？
  - 对于需要验证程序的用户，软件文档还应该包含测试用例，用例根据输入数据可分为：
    - 大多数常规数据和程序主要功能进行测试的用例。
    - 数量相对较少的输入边界用例。
    - 数量相对较少的非法数据测试用例。
  - 对于需要修改程序的用户
    - 流程图或子系统的结构图。
    - 算法的完整描述。
    - 文件规划的解释。
    - 数据流的概要描述。
    - 初始设计中，对已预见修改的讨论。
- 流程图
  - 流程图很多时候可以用直接高级语言代码表示。
- 自文档化的程序
  - 借助语言中必须存在的语句，附带尽可能多的信息。
  - 利用缩进和统一的格式提高程序的可读性。
  - 以段落注释的形式，向程序中插入必要的记叙性的文字。

## 没有银弹-软件工程中的根本和次要问题 (No Silver Bullet - Essence and Accident in Software Engineering)

- 软件工程中的根本困难
  - 复杂度，软件的复杂度是软件的必要属性，这来自于计算机的复杂性，软件系统状态的复杂性，以及复杂性随规模的非线性增加。
  - 一致性，软件的复杂度毫无规则可言，必须遵循人为惯例，随系统变化而变化，随接口变化而变化。
  - 可变性，软件由于是存粹的思维活动，因此往往随着各种应用、用户、自然及社会规律、计算机硬件等改变而被迫改变。
  - 不可见性，软件的不可见和无法可视化，增大了理解和交流的难度。
- 以往解决次要困难的一些突破
  - 高级语言，减轻了次要的软件复杂度，提高了软件生产率、可靠性和简洁性。
  - 分时，保证了及时性，提高了生产率和产品质量。
  - 统一编程环境，提供集成库、同一文件格式、提供管道和过滤器，解决了共同使用程序的次要困难。
- 银弹的希望？
  - Ada 和其他高级编程语言，Ada鼓励了现代设计和模块化概念，降低了机器的次要复杂度。
  - 面向对象编程，包括抽象数据类型和层次化类型，消除了设计表达上的次要困难，没有解决设计上的复杂度。
  - 人工智能
    - AI-1：使用计算机来解决以前只能人类解决的问题。
    - AI-2：专家系统，包含归纳推论引擎和规则基础的程序，推导逻辑结果。可以用于建议接口规则、指定测试策略、记录 bug 产生的频率、提供优化建议等。
  - “自动“编程，难以普及到广泛的寻常软件系统。
  - 图形化编程，图形难以表达复杂的软件系统
  - 程序验证，本身同样很复杂，可以减少程序测试的工作量，不能省略程序测试。
  - 环境和工具，值得尝试，能提高软件生产率和可靠性，目前汇报有限。
  - 工作站，工作站速度的提升，使得开发人员的思考成为主要活动，然而不能解决本质困难。
- 针对概念上根本问题的颇具前途的方法
  - 购买和自行开发，构件软件最可能的解决方案是不开发任何软件。购买商业软件，随着个人计算机的普及会越来越普遍
  - 需求精炼和快速原型
    - 软件系统开发最困难的是确切决定搭建什么样的系统。
    - 可以通过快速原型技术与用户达成测试一致性和可用性。
  - 增量开发，首先保证系统能够允许，然后逐步充实子系统和功能。
  - 培养卓越的设计人员
    - 尽可能早地、有系统地识别顶级地设计人员。
    - 为设计人员指派一位职业导师，负责技术成长，规划职业生涯。
    - 为设计和领导能力制订和维护职业计划。
    - 为成长中地设计人员提供相互交流和学习地机会。
