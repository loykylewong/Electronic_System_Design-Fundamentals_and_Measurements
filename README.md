# 《电子系统设计-基础和测量系统篇》理论计算用mathematica代码

## 说明

该仓库中的内容是我在写《电子系统设计 - 基础知识和测量系统篇》（电子工业出版社2021年第1版 ISBN：9787121368639）一书时，用于理论计算和图表生成的 Mathematica源代码。应部分希望深入学习的同学的要求，这里将它们开放出来，供大家参考。

The content in this repository is the Mathematica source code used for theoretical calculations and diagram generation while writing my book *Electronic Systems Design - Fundamentals and Measurements*. (CHS, ISBN:9787121368639).

## 书本内容简介(Brief Introduction of The Text Book)

本书是电子设计系列教材中的基础和测量仪器篇，侧重电路硬件，特别是模拟电路系统的基础和电学参量的测量。书中包含大量实用的电路单元，既有必要的理论推导，也给出了许多设计和装调经验，并涉及了一些现代电路系统设计相关的主题，如电源完整性概念和单电源设计技术，最后结合全国大学生电子设计竞赛赛题列举了一些电路测量系统的设计和制作案例。

全书共8章，主要内容包括信号和连接、基本元器件及应用、信号与系统基础、运算放大器及应用、其他器件及应用、基本电学量的测量原理、常用电路单元模块、经典赛题案例。

## 书本前言(Foreword of The Text Book)

笔者自2003年开始参加全国大学生电子设计竞赛培训，然后2005年参加全国大学生电子设计竞赛获一等奖，然后在华中科技大学电工电子科技创新中心担任助教，再留校担任电工电子科技创新中心专职指导教师，至今，与全国大学生电子设计竞赛已有16年之缘。笔者自幼痴迷电子技术，从第一次拿起烙铁焊接电路至今已有26年。然而，每次为刚刚学到了新东西而沾沾自喜过后，总会觉得，原来自己不懂得的还有很多，入门电子技术26年，所知或许不过皮毛。“吾生也有涯，而知也无涯”，希望同学们要谦虚好学，“以有涯随无涯，殆已！”也希望同学们学而有所成时，能学以治用，为自己、为国家、为人类社会创造价值。

这次应全国大学生电子设计竞赛官方合伙伴——美国德州仪器公司（以下简称“TI”）大学计划部的邀请，与另外三所高校的三位前辈老师一起，以电子设计竞赛为出发点，撰写电子系统设计系列教材，倍感压力与责任，唯恐不能倾尽所学，但无奈自己水平不高、书本篇幅有限，能与读者分享和一同学习的知识还有很多，只希望这本书能帮助读者牵起电子技术世界的一根线索，真正浩如烟海的知识，还需要读者自己去求索、去实践。

笔者负责的这本《基础与测量篇》主要内容是电子系统设计的基础知识和电学量的测量方法，为适应各高校电子设计竞赛培训早于相关专业课的现状，书中内容尽量不依赖《模拟电子技术基础》和《数字电子技术基础》等课程内容，而是将其中与现代电子系统设计相关的原理和内容予以总结提炼供读者学习，并不深入半导体器件内部的原理，而是重在掌握外部特性和应用电路。当然，希望读者以此书入门后，还是要认真系统地学习相关课程，夯实基础。

学习本书要求读者具有一定的电路理论基础，需要掌握基尔霍夫节点电流和环路电压定律、戴维南等效和诺顿等效定理、交流电路的相量分析法。限于篇幅，本书重心在模拟电路，未涉及系统的数字电路内容，遇到数字电路相关内容不能理解时，读者应另行参考相关书籍。微处理器系统（MCU、MPU、FPGA及软核等）及其软件也是现代电子系统设计中必不可少的内容，这部分内容已有很多适合初学者学习的书籍和公开资料，本书也不会涉及。

本书第一章主要介绍线材和连接的相关知识，并例举了一些笔者在学生培训和一些项目研发中用到的线缆、连接件供读者参考。这一章还介绍了信号完整性的初步知识并着重介绍了电源完整性的知识，这部分，特别是后者，很容易被初学者忽视，是限制初学者实践水平提升的重要障碍，望读者予以重视。

第二章主要介绍一些基础器件和应用电路，除介绍基本特性外，还重点讲述了一些对电路实现有着重要影响的特性。对于晶体管应用电路，书中也给了一定篇幅，虽然当前模拟电路系统设计看似是运算放大器的天下，但运算放大器不是万能的，在一些能用运放完成的需求中，与精妙的晶体管电路实现相比，运放实现往往也不是最优的。希望读者不要忽视培养自己晶体管电路设计的能力。

第三章是为后续章节展开不得不加入的内容，但笔者相信，它非常有用。这一章首先非常浅显地概括了信号与系统以及传输函数的概念，让读者建立起复频域分析的概念，掌握最基本的复频域分析方法，以应对后续章节的学习，至于其来源、数学原理、局限性等等，希望读者能在相关专业课程中再系统地进行学习。

第四章讲述模拟电子系统设计中最为重要的元器件——运算放大器，在简要讲述其基本原理后，重点放在了它的各种应用电路和分析和设计上，并对运放电路的稳定性和对实际电路有着重要影响的非理想特性做了较为详细的讲解。

第五章主要介绍了一些在电子系统设计中不可或缺的其它元器件，包括基本的光电器件、乘法器、锁相环、ADC和DAC等，在介绍基本原理之后，重点也在它们的应用电路设计和实现上。

第六章主要介绍了常用电学量的测量方法和原理，是第八章电子设计竞赛赛题案例讲解的重要基础。

第七章则以电路集锦的形式例举了一些在电子系统设计和电子设计竞赛中常用的和可重用性较高的电路单元模块。

第八章介绍了六个往年全国大学生电子设计竞赛赛题作品制作的案例，方案和电路基本都是从一等奖作品中提炼出来的，大多数基本原理在前面章节都已涵盖，这一章主要作用是给读者们一个参考。

水平有限，成书仓促，必有谬误，望大家批评指正！

书中的一些习惯和其它一些希望读者知悉的内容：
1. 为了便于示意和描述，一些电路图中的元器件符号在国标符号的基础上增加了一点示意性元素，例如：“ ”表示输出交流信号的电压源，“ ”表示输出脉冲信号的电压源。
2. 文中一些电路图（特别是最后两章）截取自一些不同软件的画面，部分软件中使用了非国标元器件符号，比如ANSI电阻符号：“ ”，一些元器件的标号也与国标不同，如集成电路使用“U”、三极管使用“Q”或“T”、二级管使用“D”等等。
3. 一些元器件密集的电路图中，因空间限制，电阻、电容和电感值省略了单位，但保留了必要的国际单位制词头，所有这种情况，电阻单位为“Ω”，电容单位为“F”，电感单位为“H”。
4. 许多文献资料、特别是器件的数据手册中，电压量均以字母“V”表达，但在本书的算式中，为与电压单位伏特“V”区分，一般会将代表电压量的字母替换为“U”。
5. 书中一些配图截取自国外厂商的元器件数据手册，一些图中包含英文单词或短句，请读者自行查阅（多数在正文中也会提及），我们常用的许多元器件产自国外，其数据手册和第一手资料大多为英文，阅读英文技术资料是电子设计者必备的能力。
6. 书中提到电路设计调试的经验，常常会用到 “略大于”、“略小于”之类的措辞，需要注意的是，如果是在对数刻度情景下（例如讨论频率响应、稳定性等时候），“略大于”、“略小于”可能大到数倍或小到几分之一，不应局限为正负百分之几或百分之几十。
7. 本书在很多地方给出了设计公式或者设计用的方程，在相应的电路设计时，可能需要做复杂的计算或者方程求解，笔者希望电路设计者备有能够求代数方程组数值解的计算器，如TI-83或更好的，如果有具备符号计算系统的计算器或者会使用Mathematica、Maple、Matlab Symbolic Math Toolbox等符号计算软件则更好。

非常感谢TI大学计划部对本书的支持，也非常感谢他们对全国大学生电子设计竞赛的大力支持。笔者认为，全国大学生电子设计竞赛是当今高校本、专科电类专业最权威、最客观公正和最重学科基础的竞赛，也是在全国电子行业内最具影响力的大学生竞赛，必能在各方努力和支持下，继续促进电类学科高等教育的发展，引导越来越多的学生成为优秀的电子工程师和研究者。

非常感谢电工电子科技创新中心肖看老师对我的大力支持！全书内容大纲、案例筛选都是在肖看老师帮助和指导下完成的。学生制作的部分案例和许多模块案例也是在肖看老师指导下完成的。

感谢电工电子科技创新中心大量同学参与了书中案例的设计、制作和验证！包括：2014级吴玉婷、陈耀斌、马良博、冯家祥、吴吉祥，2015级高鹏恩，2016级裘建东，2010级王德君，2012级谭昌忍，2013级胡雪欣、李琪、龙彦伯等等。还有众多参赛学生的作品方案被书中借鉴或提及，无法一一例举，一并感谢！

感谢电气学院实验教学中心尹仕老师及其他同事对我的理解与支持！

感谢TI大学计划部谢胜祥工程师在我写书期间对我的支持和鼓励！

感谢我的父母和妻子在我写书期间对我的理解、支持和无微不至的照顾。感谢我的妻子帮我修正了后两章中的许多电路图，并做了部分电路的仿真验证。感谢家中“喵喵”在我一人在家“闭关”赶稿时的陪伴和适时的“休息提醒”。
