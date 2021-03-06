# 如何开始

《软件架构探索》这个开源文档项目的是笔者对自己在软件架构方面知识的总结，它是完全免费开放的，但免费的、开源的文档并不意味着你使用它时就没有成本，也不见得这个文档中所有的内容对每一个开发人员来说都是必要的。为了避免浪费阅读者的时间和精力，笔者除了自身力求在知识点准确性和叙述流畅性方面保证质量之外，同时也在本文中简要介绍每一章的主题和所面向的读者类型，本文档各章节之间并没有明显的前后依赖关系，阅读时有针对性的查阅是完全可行的，无需一篇不漏地顺序阅读，在[此目录](/summary)中列出了各文章的明细及字数，希望有助于你制定阅读计划。

## 探索起步 <words chapter='/exploration'/>

本章面向于对架构、容器环境没有清晰概念和实战经验的初学者，它同时也是这个文档的几个示例工程的说明书，以及相应运行环境的部署手册。

假设你是一名驾驶初学者，最合理的学习路径应该是先把汽车发动，然后慢慢行驶起来，而不是马上从“引擎动力原理”、“变速箱构造”入手去设法深刻地了解一台汽车。所以，先从运行程序，看看效果，搭建好开发、调试环境，对即将进行的工作有一个整体的认知开始是很有好处的。

:::quote 提示
本文档所涉及到的工程均在GitHub上存有独立的项目，以方便构建、阅读、运行和fork。

本章中的部分内容，是由这些工程的README.md文件人工同步而来，并没有通过持续集成工具自动处理，所以可能有偶尔更新不一致的情况，如可能，建议到这些项目的GitHub页面上查看最新情况，在<a href="javascript:document.getElementsByTagName('button')[0].click()">右上角</a>有相应的超链接。如这些工程对你有用，望请不吝给个<github-button href="https://github.com/fenixsoft/awesome-fenix" data-icon="octicon-star" data-show-count="true" aria-label="Star fenixsoft/awesome-fenix on GitHub" style="position: relative; top: 4px; right: -4px;">Star</github-button> 。
:::

本章所提供的工程是作为后面所述知识的演示样例，由于数量确实不少，笔者建议并无必要一次性地把上面所有的工程都运行起来，这样很无聊。因为它们是采用不同的技术来解决同一个问题，所以每个工程执行后，最终看到的界面效果均是一样的，只是实现的架构不同。笔者的建议是不妨选择一种你目前关注的架构风格去运行起来（第一章 探索起步）、思考这种架构涉及到哪些标准方案（第二章 设计者的视角）、现在提倡的微服务、云原生解决了以前存在的哪些问题（第三章 演进中的架构），它们是如何解决这些问题的（第四、五章 核心技术支撑点与不可变基础设施）。把一个架构风格的所有内容都阅读完毕之后，再开始另一个。

## 设计者的视角 <words chapter='/architect-perspective'/>

本章面向于技术架构师。本章是整部文档的首个重点章节，也是后续的基础，介绍的是普适的架构技术、技巧与方法论，无论你是否关注微服务、云原生这些概念，无论你是从事架构设计还是从事编码开发，了解这里所列的基础知识，对每一个技术人员都是有价值的。

“架构师”这个词的外延非常宽泛，不同语境中有不同所指，本章中的技术架构师特指的是[企业架构](https://wiki.mbalib.com/wiki/%E4%BC%81%E4%B8%9A%E6%9E%B6%E6%9E%84)中面向技术模型的系统设计者，这意味着本章讨论范围**不**会涉及到贴近于企业战略、业务流程的系统分析、信息战略设计等内容，而是聚焦于贴近一线研发人员的技术方案设计者。本章将介绍作为一个设计者，你应该在做架构设计时思考哪些问题，有哪些主流的解决方案和行业标准做法，各种方案有什么优点、缺点，不同的解决方法会带来什么不同的影响，等等。以达到将“架构设计”这种听起来抽象的工作具体化、具象化的目的。

本章分为“普适问题”和“技巧专题”两部分，前者指的是每一种架构风格都需要考虑的通用问题，后者挑选了若干在微服务、云原生架构的迁移过程中较为普遍遇到的问题和解决技巧、方案。

## 演进中的微服务 <words chapter='/architecture'/>

本章面向于从单体架构转向微服务架构的开发者。

TBD

## 核心技术支撑点 <words chapter='/technology'/>

本章面向于基础设施、平台的开发者。

TBD

## 不可变基础设施 <words chapter='/immutable-infrastructure'/>

本章面向于基础设施、平台的开发者。

TBD

## 附录 <words chapter='/appendix'/>

本章面向刚开始接触云原生环境的设计者、开发者。

这一章内容主要是云原生环境搭建和程序发布过程，原本它们并不属于笔者准备讨论的重点话题，至少没有到单独开一章的必要程度。但由于容器化的服务编排环境本身构建、管理和运维都有一定的复杂性，尤其是在国内特殊的网络环境下，无法直接访问到Google等国外的代码仓库，以至于不得不通过手工预载镜像或者代理的方式来完成环境搭建。为了避免刚刚接触这一领域的读者在入门第一步就受到不必要的心理打击，笔者专门设置了这个目录章节。这章与其他几章讨论设计思想、实现原理的风格差异很大，它是整部文档唯一的讨论具体如何操作的内容。

肯定有相当一部分读者这章的内容本身就是了解的，这部分读者建议无需仔细阅读，在有需要的时候，可当作工具查阅。



