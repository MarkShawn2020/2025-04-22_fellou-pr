

```insta-toc
# 本文目录：

- 降智与否的对比
- 降智的直观表现
- 降智的条件背景
    - 1. 2024年11月初：降智现象初现
    - 2. 2024年12月初：降智问题引发广泛讨论
    - 3. 2024年12月中旬：降智蔓延至全客户端
- 我采用的降智测试
    - 测试一：工具调用
    - 测试二：封面生成
- 实锤：scamalytics.com 的 IP 健康度与账号没有关系
- 实锤：Pow（工作证明量）也和降智与否关系不大，手机 web 版也无法防止降智
- 关于 ChatGPT 降智的核心影响因子排序
```
## 降智与否的对比

先直观感受一下降智与否对输出的影响，这在 gpt-4o 支持最新的生图功能后，与上一代的 dalle 效果差异极大（犹记得一两年前我们还在微信机器人内接 dalle 模型很开心，当时还没朋友吐槽了，其实实在不能看）。

![image.png](https://poketto.oss-cn-hangzhou.aliyuncs.com/20250414131658.png?x-oss-process=image/resize,w_800/quality,q_95)

很显然，正常版生图的效果，已经达到生产可用级别，我已经大量用于文章封面、插图生成了，在那之前用的是 midjourney，再在那之前则是用的 canva 或者找平面设计师。

这一波，初级平面设计师真地哭晕在了厕所，不得不厚葬了。

## 降智的直观表现



![[chatgpt-dalle.mp4]]



## 降智的条件背景

### 1. **2024年11月初：降智现象初现**

- **表现**：部分用户发现ChatGPT回答质量下降，表现为直接输出答案（不显示思考过程）、无法解析图片/文件、拒绝调用联网搜索等高级功能。
- **影响范围**：主要针对使用代理工具访问ChatGPT的用户，尤其是IP地址被标记为高并发的群体。
- **原因推测**：OpenAI因算力资源紧张和训练数据不足，开始将部分用户的底层模型从GPT-4o替换为低算力版本（如GPT-4o mini或GPT-3.5），以节省资源。

---

### 2. **2024年12月初：降智问题引发广泛讨论**

- **用户反馈激增**：大量用户报告类似问题，确认"降智"已从个别案例发展为系统性现象。
- **功能限制扩展**：除模型替换外，高级功能（如联网、文生图）被进一步限制，部分用户即使开通Plus会员也无法使用。
- **官方应对措施**：OpenAI向高使用量开发者免费发放API token（每日1100万tokens），以换取数据共享权限，缓解训练数据短缺问题。

---

### 3. **2024年12月中旬：降智蔓延至全客户端**

- **影响范围扩大**：降智行为从网页端和Windows客户端扩展至手机App、Mac客户端等全平台，所有用户均可能受到影响。
- **核心原因明确**：OpenAI公开承认算力资源紧张，尤其是GPT-4o高算力版本单任务消耗超1000美元资源，远超旧版本（GPT-4为5美元/任务）。
- **用户应对策略**：社区提出通过优化IP质量（如使用低并发IP）、切换账号或客户端版本等方式缓解问题。

---

## 我采用的降智测试

我搜寻了一些测试方法。

有一种办法是测试一道数学题或者日语题，但我感觉太麻烦了，没有兴趣。

还有一种办法是先发一张图片据说就能解封，但我实测是没用的（也可能是失效了）。

我目前采用如下两种办法进行降智测试。

### 测试一：工具调用

第一种，是在 `gpt-4o` 模式下，询问：「**summarize your tool in a markdown table with availability**」。

这个问题在很多个教程里都有提（比如：[ChatGPT被"降智"怎么办？O1不思考，4o不能联网、分析图片和处理文件！](https://www.youtube.com/watch?v=uQ8ExarQhyM)），确实有效。

对比如下：

![image.png](https://poketto.oss-cn-hangzhou.aliyuncs.com/20250414151512.png?x-oss-process=image/resize,w_800/quality,q_95)

值得注意的是，有很多教程说，当工具调用低于 4 个的时候是降智，这个也是一种过时的说法，因为工具肯定会越来越多。

但总体原则是很简单的：**账号越尊贵/健康，则能调用的工具越多、且越高级；尤其是越高级的工具，越贵，越要做限制**。

在目前（2025年04月14日）gpt-4o 下最贵也最火的工具场景就是 gpt-4o 的文生图能力（`image_gen`，参考： [GPT-4o「吉卜力风」一夜爆火，奥特曼连夜换头像！宫崎骏痛批AI侮辱生命](https://mp.weixin.qq.com/s/9qzPALAmXmIaMPu7TuaRuQ)），所以可以把这个工具的有无当做是否降智的标准之一。

### 测试二：封面生成

第二种非常实用（独创），就是给定我的一篇文章，然后让 gpt-4o 给我输出一个封面。

使用 dalle 和使用 gpt-4o 生成的图片风格差异很大（尤其是在饱和度、布局、文本内容上）。

![image.png](https://poketto.oss-cn-hangzhou.aliyuncs.com/20250414152215.png?x-oss-process=image/resize,w_800/quality,q_95)

## 实锤：scamalytics.com 的 IP 健康度与账号没有关系

在账号健康、使用 Mac 客户端的情况下，目前唯一能影响是否被降智的因素就剩 IP 了。

我原先也非常下意识地认为 scamalytics.com 的 IP 健康度 将与减少降智的几率呈显著的正向关系。

于是，我为了快速地选出最健康的 IP，我让 cursor 给我写了一个较为复杂的程序，它会自动遍历我们 clash 配置文件里的 vmess 节点列表，然后自动解析出具体的 IP，再自动地查询 scamalytics.com 以获得健康度，最终汇总成表格。

以下是对 cursor 的核心 prompt：
```md
@config.yaml:L29-30
当 proxy 设置为 阿根廷 A 时，网站显示 ip 是 82.152.6.214  
当设置为韩国 A 时，显示是 125.240.80.85  
想知道我们怎么从这个配置文件程序化地得到 ip

---

@get_real_proxy_ip.py 似乎是可行的，但是得一个个手动切换 proxy，这个不适合批量

---

再得到 ip 之后，再增加一个风险指数检测，例如访问 https://scamalytics.com/ip/125.240.80.85 ，会在源代码里得到：  
  
{  
  
"ip":"125.240.80.85",  
"score":"50",  
"risk":"medium",  
"is_blacklisted_external": false,  
...  
}  
  
将其信息提取出来
```

核心程序开源在： git@github.com:MarkShawn2020/2025-04-14_ip-research.git

然后基于我的某个付费服务商 A 进行测试，得到了一张表格：

```shell
python proxy_ip_cli.py -c data/config_miaomiao.yaml  -a -f both
```

![image.png](https://poketto.oss-cn-hangzhou.aliyuncs.com/20250414124801.png?x-oss-process=image/resize,w_800/quality,q_95)

结果我从风险度最低为 0 的台湾、美国，到超过 10 的台湾、到 100 的土耳其，全都通过了降智测试……

**我非常困惑！**

于是，我又对我的另一个免费服务商 B 进行测试，得到了另一张表格：

```shell
python proxy_ip_cli.py -c data/config_bitz.yaml  -a -f both
```

![image.png](https://poketto.oss-cn-hangzhou.aliyuncs.com/20250414124836.png?x-oss-process=image/resize,w_800/quality,q_95)

结果大失所望！

第二张表里即便是风险度为 0 的 结点 / IP，也完全无法通过测试！

![image.png](https://poketto.oss-cn-hangzhou.aliyuncs.com/20250414155002.png?x-oss-process=image/resize,w_800/quality,q_95)


基于此，我很明确得到了一个非共识：

**降智与否与 scamalytics.com 网站的 IP 风险度没有任何关系**。

**ChatGPT 确实会考虑 IP 的问题，但是 scamalytics.com 还没有资格做这个判官。**

## 实锤：Pow（工作证明量）也和降智与否关系不大，手机 web 版也无法防止降智

具体就不展开了，但很确信，不构成有效条件

![image.png](https://poketto.oss-cn-hangzhou.aliyuncs.com/20250414155455.png?x-oss-process=image/resize,w_800/quality,q_95)


## 关于 ChatGPT 降智的核心影响因子排序

| 推荐程度 | 解决方案    | 具体操作                                      | 实测效果                                        |
| :--: | :------ | :---------------------------------------- | :------------------------------------------ |
| ⭐⭐⭐  | IP 第一   | 选择独享/优质IP节点，避免共享IP                        | 有效。正常付费节点（有`image_gen`工具）                   |
|  ⭐⭐  | 账号第二    | 重新注册并付费一个新号                               | 成本较高，但在确保前两者的情况下一定有效                        |
|  ⭐⭐  | 客户端第三   | 使用Mac桌面版/移动端                              | 有效。Mac/iOS客户端稳定，其他平台未测试                     |
|  ⭐   | 优化账号信息  | 清除浏览器缓存或重新登录                              | 部分有效。可临时恢复部分功能                              |
|  ⭐   | 优化网络环境  | 使用Cloudflare Warp等工具改善IP质量                | 效果不确定。需视具体IP情况而定                            |
|  ⭐   | 使用镜像站   | 通过第三方镜像站访问                                | 测试显示镜像站账号（黑卡）功能受限                           |
|  ⭐   | 验证方法    | POW值验证：查看`proofofwork.difficulty`超过004e20 | 可作为参考指标，但非决定因素                              |
|  ⭐   | 验证方法    | 工具检测：正常应显示4个以上工具                          | 可靠的降智判断标准，特别是`image_gen`工具的存在               |
|  ⭐   | 验证方法    | 日文测试题：未降智需5分钟以上思考                         | 较为主观，但可作为参考                                 |
|  ❌   | 切换客户端版本 | 网页版F12开发者工具切换移动端视图                        | 无效或已失效。                                     |
|  ❌   | 优化账号信息  | 清除浏览器历史记录                                 | 无效且有害。                                      |
|  ❌   | 验证方法    | 安装「ChatGPT Degrade Checker」扩展             | 无效且有害（因为使用了第三方接口）。                          |
|  ❓   | IP风险评估  | 通过scamalytics.com衡量IP风险                   | 实测证明：**降智与否与scamalytics.com网站的IP风险度没有直接关系** |

**结论：** 最有效的方法是使用**优质的账号**（非共享、非多 IP、尽量不多开）、优**质专线 IP**和**稳定的客户端**（如Mac版或移动端，而非网页版）。

此处，插一嘴，某种意义上，如果通过镜像站固定住账号、IP，甚至客户端，也许确实会比官方账号更稳定（前提是量不大，量大了，千斤都顶不住：）

ok，本期研究到此为止，如果您还有什么问题，欢迎联系我（vx：youshouldspeakhow），祝您工作顺利！
