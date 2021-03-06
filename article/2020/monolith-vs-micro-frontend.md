> * 原文地址：[Monolith vs. Micro Frontends](https://blog.bitsrc.io/monolith-vs-micro-frontend-e6e9772a068b)
> * 原文作者：[Florian Rappl](https://medium.com/@FlorianRappl)
> * 译文出自：[掘金翻译计划](https://github.com/xitu/gold-miner)
> * 本文永久链接：[https://github.com/xitu/gold-miner/blob/master/article/2020/monolith-vs-micro-frontend.md](https://github.com/xitu/gold-miner/blob/master/article/2020/monolith-vs-micro-frontend.md)
> * 译者：[zenblo](https://github.com/zenblo)
> * 校对者：[Usualminds](https://github.com/Usualminds)、[regon-cao](https://github.com/regon-cao)

# 单体应用与微前端开发对比

你是现代主义者吗？你的 web 应用是跟随现代潮流的吗？那你必定是在做微前端！挺激动人心的不是吗？

![](https://cdn-images-1.medium.com/max/3840/1*YaRaJ3Sxh9KNcxMZsr7ofg.jpeg)

所有的复杂性、所有的麻烦，为的是什么？几个月后你的前端应用就过时了，你应该把时间精力花在可重用组件上。“没有什么能打败单体应用开发！”这是种相当狭隘的观点。

你可能赞成第一种或第二种观点。然而，在实际软件开发中，答案总是在它们之间。

> 看情况！

认识我的人都知道我是**单体应用开发的忠实粉丝**。同时，最近我在微前端上做了很多开发，我甚至创建了一个[名为 Piral 的精巧框架](https://github.com/smapiot/piral)提供创建大型微前端解决方案。即使在这里，我们也不是盲目地提倡在未知开发情况下使用该方案。

## 使用单体应用开发的理由

许多人认为，应根据应用程序的大小来决定使用单体应用还是微前端开发。我不怎么认同这种方式。当然，如果应用程序非常小，则有可能将重构时间缩短到使其他所有项目看起来都费时冗余的水平。但是，对我而言真正的考量指标是业务角度。

如果是静态的应用程序，没有那么频繁地更新，并且具备了向所有用户推送的功能，那么整体来看单体应用开发方案是一个不错的选择。

小型的单体应用是比较容易开发、部署和测试。当然，对于单体应用而言，这没有什么特别的。任何小规模且专注于单一业务的系统都是易懂的。

简而言之：

* 一致
* 可靠
* 性能

## 使用微前端开发的理由

微前端应该是只有大企业才能驾驭的巨型应用。虽然所有这些属性都支持使用微前端，但它们不是必需的。如果合适的话，即使是一个小型应用程序也可以从微前端开发中受益。例如，我们可能有一个登录页面应用程序，它每天都需要更新一些内容。当然，我们可以将这个连接到后端处理，但是就为了发布一个(可能非常普通的)内容片段，突然之间我们需要维护很多东西。相反，将其作为前端组件发布并直接使用可能是很好的解决方案。

对于大型应用程序，我们要担心的是“遗留问题”。包含遗留代码或者不能使用最新最好的工具都会使软件项目最终失败。要么是错过了关键的更新，要么是未能吸引到新的开发人员。微前端支持项目中使用多个不同的技术栈，提供了一种很好的解决方案。

![Micro frontends can outperform their monolithic ancestors — given the right problem statement.](https://cdn-images-1.medium.com/max/2000/1*iVLtTGNKeVjX3p2dmtPmRA.png)

微前端解决方案在很多方面都很灵活。因此，与传统前端相比，它面临着各种挑战。如果这些挑战（性能或一致性等）得到解决，那么微前端就不一定比单体应用方案更复杂。实际上，单个部分（即真正的微前端）更容易理解和维护。事实上，这能大幅减少加载时间，是对开发人员更加友好的解决方案。

简而言之：

* 可扩展
* 灵活
* 独立

## 结盟与合作

那么不同的团队组织最适合哪种模式呢？显然，微前端允许更多的分布式团队，而单体应用需要大量的规整校对，通常适合一个遵循严格层次规范的集中式团队。当然，也有例外的情况，但在大多数情况下，事实与上述观点非常接近。

根据微前端应用程序的实际架构，可能会有一个集中式团队负责跨技术栈的问题处理。其余团队可以被认为是辅助团队，规模从 1 到 5 个开发人员，这取决于项目分工。几乎不需要调整，大概需要来自企业高层管理或核心团队的一些微调。每个辅助团队都可以按照自己的计划表工作，准备好了就发布应用。

![Different teams producing different artifacts.](https://cdn-images-1.medium.com/max/2000/1*TM5WFttKghAGLdcZ02sv2w.png)

相比之下，单体应用由一个独立团队开发，或者一个大的中心团队负责主功能，部分功能由小团队开发。然而，在任何情况下都会有规整校对。有一种情况是，辅助的团队规模实际上也相当大，并且有自己的流程。这就是像 nexus（Maven 仓库管理器）或大规模敏捷团队（scrum of scrums）概念出现的地方。一旦我们听到这些术语，我们就知道正在发生大量的规整校对，正在进行很多会议，导致效率大幅下降。

![One large team producing a single application.](https://cdn-images-1.medium.com/max/2000/1*Sj8vdinS7TjOb48sb7-5qQ.png)

效率的损失起初听起来像是一个缺点，但是请记住，随着时间的推移，每个成熟的应用程序都会有开发效率的损失。这是很正常的，甚至在某种程度上是人们所期望的。毕竟，这意味着真正的客户正在使用该产品，并且这些调整变化需要经过深思熟虑。因此，和往常一样，问题不在于“是否存在低效率”，而在于这个过程“有多低效率”。

## 项目部署

这两种开发模式最关键的一点是如何进行项目部署。我见过同时部署全部项目的微前端解决方案。每个微前端都在一个大的持续集成、持续交付（CI/CD）中发布。我是坚决反对这种模式。

如果我们一次发布所有内容，那么真正的微前端解决方案并不理想。它可能适合在 monorepo 模式中使用可重用包非常有效地开发单体应用，但不是微型前端。

联合发布会让我们失去什么？

* **独立** （团队需要发布，他们需要准备发布...）
* **缓存** （所有资源都在相同时间失效，而不是在实际发生变化时失效）
* **效率** （我们需要对发布日期进行一些调整，这意味着额外的低效率）

做联合发布好处是什么？

* **一致** （我们知道所有部件都已更新到最新版本）
* **可靠** （我们可以只进行一次辅助测试就知道一切正常）
* **稳定** （应用程序将只在特定的时间间隔内更新，而不是经常变化）

> 虽然微前端可以在两种极端情况下使用，但整体将主要保留在较大的联合版本中。

微前端也可以混合部署。例如，我们可以有一些由一个到多个团队开发的核心微前端，这些核心微前端可以联合部署。这种混合模式可能是一个很好的折衷方案，旨在避免损失效率、独立性和缓存能力，同时保持一致、可靠和稳定。这在移动操作系统（或者实际上是大多数操作系统）中已经非常成熟：

* 第三方应用程序有自己的发布周期
* 部分核心应用程序可能会独立
* 随着主要操作系统发布更新，核心应用程序也有版本更新

从某种意义上说，一个完整运行的微前端解决方案，可以被视为一个移动应用程序。能够调整部署策略是微前端的优势之一。

## 结论

在单体应用和微前端开发之间进行选择并不困难。通常，我们无需考虑太多就可以从单体应用开始。一旦需要，仍然可以使用微前端解决方案。

然而，这两种方案各有利弊。我们应该努力找到能解决我们问题的合适方案。如果那是单体应用——太好了！如果我们最终采用微前端开发——那也太好了！

不用顾虑别人告诉你什么是流行的技术方案，什么是最佳实践。思考问题的真正困难之处，并尝试提出最佳解决方案。除了从技术和商业的角度考虑，团队组织（团队中每个人的背景，他们对不同解决方案的接受程度等）也绝不应该被忽视。

> 如果发现译文存在错误或其他需要改进的地方，欢迎到 [掘金翻译计划](https://github.com/xitu/gold-miner) 对译文进行修改并 PR，也可获得相应奖励积分。文章开头的 **本文永久链接** 即为本文在 GitHub 上的 MarkDown 链接。

---

> [掘金翻译计划](https://github.com/xitu/gold-miner) 是一个翻译优质互联网技术文章的社区，文章来源为 [掘金](https://juejin.im) 上的英文分享文章。内容覆盖 [Android](https://github.com/xitu/gold-miner#android)、[iOS](https://github.com/xitu/gold-miner#ios)、[前端](https://github.com/xitu/gold-miner#前端)、[后端](https://github.com/xitu/gold-miner#后端)、[区块链](https://github.com/xitu/gold-miner#区块链)、[产品](https://github.com/xitu/gold-miner#产品)、[设计](https://github.com/xitu/gold-miner#设计)、[人工智能](https://github.com/xitu/gold-miner#人工智能)等领域，想要查看更多优质译文请持续关注 [掘金翻译计划](https://github.com/xitu/gold-miner)、[官方微博](http://weibo.com/juejinfanyi)、[知乎专栏](https://zhuanlan.zhihu.com/juejinfanyi)。
