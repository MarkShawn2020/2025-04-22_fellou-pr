---
title: "Fellou浏览器全面深度测评"
subtitle: "V0.1.0"
date: 2025-04-23
author: [南川]
lang: "zh-CN"
titlepage: true
titlepage-color: "5D1EB1"         # 飞脑科技主紫色
titlepage-text-color: "FFFFFF"
titlepage-rule-color: "FFE600"    # 强调黄作为分隔线
titlepage-rule-height: 2
titlepage-logo: /Users/mark/飞脑科技/assets/branding/cs-magic_logo_white_1280.png
---

# AI与浏览器的强强联合：Fellou浏览器全面深度测评

*文章撰写于2025年4月23日，南川*

![Fellou 浏览器](./cover.png)

近期，AI浏览器赛道持续火热，Dia、Manus、Arc Search等产品纷纷入局，试图重新定义我们与互联网的交互方式。而今天我们要聊的主角——Fellou浏览器，以其独特的AI Agentic技术为核心，正在尝试将浏览器从"信息获取工具"进阶为"自动化任务执行助手"。

经过我们团队一个月的实测，今天这篇文章将从多个维度深入剖析这款产品的优劣势，以及它对未来浏览器形态的启示。无论你是AI产品爱好者，还是正在寻找提升工作效率的方法，这篇分析都值得你读完。

## 一、产品定位与核心功能

Fellou浏览器并不是简单地在传统浏览器中嵌入AI对话框，而是从底层重构了浏览器与AI的交互逻辑。它的核心卖点是自动化操作网页的能力，以及对信息的深度整合与呈现。

官方宣传中，Fellou提供四大核心功能：

1. **自动化任务**：模拟用户操作完成特定任务，如自动发推文、数据采集等
2. **网页总结**：快速理解和提炼网页内容的核心信息
3. **深度研究(Deep Search)**：自动搜索并整合多个来源的信息，生成结构化报告
4. **镜像空间**：在云端虚拟环境中执行操作，不占用本地资源

经测试，这些功能在现实场景中的表现如何？我们团队找来了不同背景的7位测试者，横跨AI工程师、产品经理、内容创作者等角色，针对各类实际应用场景进行了为期一个月的全面测试。

## 二、亮点功能实测：它能做什么？

### 1. Deep Search：信息提取的极致体验

如果说传统搜索是"给你一堆砖头"，那Fellou的Deep Search则是"直接给你一栋盖好的房子"。它不仅能够搜集信息，更能将信息组织成一份可视化程度极高的报告。

我们让Tiger（测试者之一）针对"MacBook Air与MacBook Pro对比"进行了深度搜索，3分钟后，Fellou生成了一份包含规格参数、价格对比、使用场景分析的完整报告。更令人惊艳的是，报告采用了多标签页设计，配有交互式图表，视觉呈现效果堪比专业设计。

**亮点分析**：
- 信息获取速度快（平均3-4分钟）
- 报告视觉呈现极佳，多标签页+交互式图表体验流畅
- 同时启动5个影子空间并行工作，提高效率
- 内容组织结构清晰，重点突出

测试者洪楠在《消费决策场景》测试中给出了8-9分的高分评价："信息比较完整，比较维度丰富，购买建议针对不同决策侧重点提供了选择"。

然而，信息质量上确实存在一些问题。乐阳在测试中发现，Deep Search偶尔会产生"幻觉"内容，特别是在一些专业领域。比如生财有术社群的会员构成数据，被测试者质疑为AI生成而非真实数据。

### 2. 自动化任务：AI驱动的"操作工"

Fellou最有野心的功能是自动化任务执行。在我们的测试中，它确实展现出了一定的自动化能力：

- **社交媒体自动操作**：能够登录Twitter账号并发布推文
- **数据采集**：可以爬取特定网站的内容并整理成结构化数据
- **内容发布**：能够在各平台自动填写表单并提交内容

AJ（测试者之一）成功让Fellou自动关注了一篇文章中提到的所有Twitter账号："它能识别出文章中的博主信息，逐个打开链接，判断是否已关注，然后自动跳过已关注的账号，继续执行下一步。整个流程像是一个训练有素的虚拟助理。"

不过，自动化能力仍有明显局限：
- 遇到反爬虫机制时任务容易失败
- 执行速度相对缓慢，简单任务不如手动操作
- 需要频繁人工介入（如登录、验证码等）
- 执行操作时无法切换到其他标签页（这严重影响了"自动化"的实用性）

测试者田乙豆指出："屏幕远程控制比竞品更加顺滑，开放多浏览器窗口的操作效率高，但在人物搜索完整性、密码管理、验证处理等方面存在缺陷。"

### 3. 网页总结：快速理解内容

网页总结功能相对简单直接，但在测试中表现相当稳定：

- 学术论文总结：能够提取研究方法、结论和关键发现
- 新闻内容提炼：能够识别事件主体、时间线和关键信息
- 多语言输出：支持将内容翻译为指定语言后再总结

测试者张巧对比了Fellou与豆包在内容生成上的差异，发现Fellou在总结质量上与其他AI工具相当，但没有显著优势。

### 4. 学术研究场景：准确性是硬伤

我们特别安排了算法工程师洪楷对Fellou在学术场景下的表现进行测试，结果有些令人失望：

- Google Scholar搜索时产生严重的内容幻觉问题，搜索结果可信度低
- Arxiv搜索结果真实性较高，但无法完全按照指令获取指定数量的文献
- 无法突破学术平台的反爬限制，数据获取不完整

洪楷给出了5-6分（满分10分）的评价："相比其他Agent产品，在处理学术平台的登录和验证方面更进一步，但信息准确性问题严重，幻觉内容多。"

## 三、与Dia浏览器的对比：各有所长

为了更客观地评估Fellou的价值，我们安排了Yuki对Fellou与当前热门的Dia浏览器进行了横向比较。

**1. 个性化体验**
- Dia：提供用户个性化设置，包括偏好导入、回答风格选择
- Fellou：尚未提供个性化定制，体验相对标准化

**2. 功能多样性**
- Dia：提供两种模式（常规搜索引擎模式和对话模式）
- Fellou：提供四种模式（常规搜索、对话、Deep Search、自动任务）

**3. 自动化能力**
- Dia：不具备独立操作网页和模拟浏览的能力
- Fellou：能通过镜像空间操控浏览器自动搜索和操作网页

**4. 搜索质量**
- Dia：搜索结果质量和准确性相对更高
- Fellou：搜索范围广，但准确性有待提高

**5. 浏览器基础功能**
- Dia：常规浏览器功能完善
- Fellou：基础浏览器功能不足，如缺少传统地址栏和书签管理

**6. 内容呈现**
- Dia：内容以对话形式呈现，更加简洁
- Fellou：报告呈现形式丰富，多标签页+交互式图表获得好评

Yuki的总结是："Fellou在Deep Search的呈现效果上独树一帜，报告视觉质量很高，但内容准确性和基础浏览器功能都不及Dia。"

## 四、优劣势分析：为何值得关注，又为何难以满足所有人

### 优势与亮点

1. **AI驱动的自动化能力**：能够模拟用户操作完成特定任务，这是Fellou最大的差异化优势
   
2. **深度研究功能的呈现效果**：报告以多标签页和交互式图表呈现，用户体验流畅，是目前所有同类产品中视觉呈现最佳的
   
3. **任务并行处理能力**：同时启动多个影子空间处理任务，效率较高
   
4. **网页总结的多语言支持**：能够有效总结网页内容，支持多种语言输出
   
5. **消费决策辅助表现出色**：在商品调研和购买决策场景下信息整合全面，购买建议具有针对性

### 存在的问题与不足

1. **基础浏览器功能不完善**：缺少常规浏览器功能，如地址栏、标签管理、书签等基础功能
   
2. **新标签页交互不直觉**：新开标签时弹出的对话框被多位测试者认为干扰操作流程
   
3. **数据质量和内容准确性**：特别是在深度研究功能和学术搜索场景中，信息准确性有待提高
   
4. **任务执行稳定性**：部分复杂任务执行中途失败或结果丢失，特别是遇到反爬限制时
   
5. **后台执行限制**：执行操作时无法切换到其他标签页，降低了"自动化"的实用性
   
6. **学术研究内容幻觉**：在学术场景中，存在严重的内容编造问题

## 五、应用场景测评：它适合谁？

通过多位测试者的实际体验，我们发现Fellou在不同场景下的表现差异很大。

### 最佳应用场景：消费决策

测评得分：**8-9分（满分10分）**

在消费决策场景下，如商品调研和购买决策，Fellou表现出色：
- 信息收集全面
- 对比维度丰富
- 购买建议针对不同需求提供选择
- 视觉呈现直观易懂

洪楷的测试案例"衣物毛球修剪器调研"中，Fellou提供了多个品牌的详细对比，价格和型号基本准确，为不同预算和需求的用户提供了分类建议。

### 一般应用场景：信息收集

测评得分：**7分（满分10分）**

在LinkedIn信息提取、社交媒体内容分析等场景下：
- 信息采集速度较快
- 能处理多种网站格式
- 但信息收集不够完整，存在疏漏

田乙豆指出："屏幕远程控制比竞品更顺滑，开放多浏览器窗口的操作效率高，但在人物搜索和内容提取方面存在疏漏。"

### 不推荐场景：学术研究

测评得分：**5-6分（满分10分）**

在学术论文搜索和整理、专业学术研究场景下：
- Google Scholar搜索存在严重内容幻觉
- 无法按指令获取足够数量的文献
- 信息准确性问题严重

洪楷的测试表明，尽管Fellou在处理学术平台登录和验证方面有所进步，但内容准确性问题使其不适合专业研究使用。

## 六、产品定位思考：浏览器还是Agent？

经过一个月的深入测试，我们发现Fellou的产品定位存在一定模糊性。Tiger在测试报告中提出了一个很有见地的观点：

> "当前阶段的Fellou更像是'具有浏览网页能力的agent产品'，而非完整的浏览器。"

这一定位混淆也直接导致了用户体验上的分裂：

- 作为浏览器：缺少基础功能，如地址栏、书签管理等
- 作为Agent：自动化能力有限，需要频繁人工介入

这种定位不清可能是Fellou目前面临的最大挑战之一。用户究竟是把它当作主力浏览器使用，还是作为特定任务的辅助工具？我认为，Fellou团队需要在这一点上做出明确选择。

## 七、用户体验痛点：阻碍全面应用的关键因素

通过7位测试者的反馈，我们归纳出几个最关键的用户体验痛点：

### 1. 新标签页体验差

AJ在测试中特别提到："当我想要点击加号开启一个新tab页面的时候，默认跳出一个浮动的弹框页面，想让我输入指令和内容。其实我就只是想开个新页面而已，给我这个选项好不好。"

这种强制性的交互设计，违背了用户的基本使用习惯，造成了不必要的摩擦。

### 2. 地址栏缺失

作为一款浏览器，Fellou缺少传统的地址栏，这使得直接输入URL变得不便。多位测试者表示，这是他们无法将Fellou作为主力浏览器使用的主要原因之一。

### 3. 报告保存问题

乐阳发现了报告保存和恢复的缺陷："有时候生成的报告打不开，同时我们也观察到报告的生成时间有时候很长。"

洪楷也提到："在同一个对话里提了其他要求后，之前的报告在fellou系统上就看不到了..."

这种不稳定的内容保存机制，无疑会影响用户对产品的信任。

### 4. 后台执行限制

执行自动化任务时，Fellou要求用户保持在当前标签页，不能切换到其他页面，这严重限制了"自动化"的价值。如果用户需要盯着屏幕看AI完成任务，那与手动操作相比，优势就大大减弱了。

## 八、改进建议：如何让Fellou更好？

基于测试结果，我们为Fellou团队提出以下改进建议：

### 1. 完善基础浏览器功能

- 增加传统地址栏和书签管理
- 改进标签页管理体验（尤其是新建标签页的流程）
- 增加扩展插件支持

### 2. 提升内容质量

- 扩充搜索数据源
- 优化内容准确性评估机制
- 增加内容筛选和事实核查功能
- 提供信息源引用和链接

### 3. 增强自动化能力

- 提高自动化任务的执行速度
- 支持后台执行，允许用户同时进行其他操作
- 增强对反爬机制的应对能力

### 4. 改进用户体验

- 优化新标签页体验
- 提供更细粒度的语言和输出偏好设置
- 改进会话保存和恢复机制

### 5. 学术功能优化

- 强化对学术内容的准确性检查
- 改进与学术平台的交互能力
- 提供引用格式和文献整理功能

## 九、结论：Fellou的未来在哪里？

Fellou作为一款基于AI Agentic技术的浏览器，展现出了强大的自动化能力和信息整合能力，特别是在深度研究和报告生成方面的交互设计令人印象深刻。然而，作为浏览器，其基础功能的缺失严重影响了整体用户体验，同时内容质量和数据准确性有待提高。

我认为，Fellou代表了浏览器进化的一个重要方向——从被动的信息展示工具，向主动的任务执行助手转变。这种转变既有机遇也有挑战：

**机遇在于**：Fellou的自动化能力和报告生成功能确实解决了现实痛点，特别是在信息过载的时代，能够快速提炼有价值信息并生成可视化报告的功能非常有吸引力。

**挑战在于**：要在保持创新性的同时，不能忽视用户的基本使用习惯。浏览器作为日常工作的核心工具，其基础功能和稳定性是用户体验的基石。

如果Fellou能够在下一版本中解决基础浏览器功能缺失、内容准确性和自动化任务稳定性等问题，它有潜力成为重塑我们互联网使用方式的重要产品。

最后，我想用测试者Tiger的一句话来总结Fellou的现状：

> "Fellou不是一款完美的浏览器，但它展示了浏览器与AI深度融合的可能性。它让我们看到，浏览器不仅可以是信息的窗口，还可以是解决问题的助手。"

在AI与浏览器的融合之路上，Fellou无疑是一个大胆的探索者。尽管还有不少问题需要解决，但它已经向我们展示了未来浏览器的一种可能形态。

---

*本文基于7位测试者在1个月内对Fellou浏览器的全面测试结果编写，测试覆盖了日常使用、专业研究、自动化任务等多个场景。如需了解更多测试细节，请联系作者。*
