  

## 个人背景

算法工程师, 常年需要跟踪视觉任务和时间序列预测任务的论文情况

## 测试用例, 在google scholar上进行文章信息搜集

- 场景描述
    
    - 在google scholar上对指定关键词在指定时间段进行搜索, 对搜索结果进行搜集
        
- 测试步骤
    
    - /fellou 要求fellou执行以下prompt, 帮我从google scholar上发现标题内容包含time series forecasting的文章, 2024年发布的, 给出这些文章的标题, 作者, 链接, Abstract, 并且把Abstract翻译成中文, 对这些文章进行深入分析, 对他们使用的方法, 适用的数据集进行分析和展示
        
- 观察与数据
    
    - 能形成一份看起来完整的报告 https://chat.fellou.ai/report/a6dfab3f-685e-4788-8b1e-820e8129bb23
        
    
    ![](https://acnx3ilalybs.feishu.cn/space/api/box/stream/download/asynccode/?code=OTdjMGE4YzBhYjAzNzVjMGUyYmY0YjRlMmRjMzJjMmRfN3YwQk5YajRXMFpUYnFDb1JCaHQ3TTluM0FSemlRVkxfVG9rZW46UmVxRGJyRnJYb00zbWN4MzI0S2NQaW1mbkloXzE3NDUzMzM4OTE6MTc0NTMzNzQ5MV9WNA)
    
    - 报告内涉及的所有文章均为幻觉
        
    
    ![](https://acnx3ilalybs.feishu.cn/space/api/box/stream/download/asynccode/?code=YWExNzM2M2MyZTMxZmRmZGUyZjE1ODU3NGMxYzdiMmVfdExGWU53RnBOYnJleGVpSGJMTGd1d0VWak5uVXVCRWRfVG9rZW46Wmt6WmJSQXNJbzN4Nk54VkxxZGNaS3V6bjlmXzE3NDUzMzM4OTE6MTc0NTMzNzQ5MV9WNA)
    
    ![](https://acnx3ilalybs.feishu.cn/space/api/box/stream/download/asynccode/?code=NzkzZDczNjhjOWM1ZTMwN2MzZmMzN2Y2YTZiNGU0NjZfVXByTGxiM2Exb0o0elg4QWV4VHJkaThieGIzblpLeEVfVG9rZW46QzZNZGJNc01ob3E1anh4WGprdGNUaUV4blNiXzE3NDUzMzM4OTE6MTc0NTMzNzQ5MV9WNA)
    
    - 从数量上只采集了10篇(均为幻觉), 实际上这个关键词的搜索结果超过20000篇, 另外我们还用其他测试用例尝试强制要求采集50篇, 最后的结果只采集了20篇(也均为幻觉), 所以这里同时存在指令跟随能力和幻觉方面的问题, 我猜测应该也有页面信息采集的时候发生了反爬问题
        
- 优势亮点
    
    - 相同的情况我们也测过Manus, Grok, 其实也得不到良好的结果, 但是Fellou起码有在让我处理登录或者人机验证的过程, 看起来比其他agent是更往前走了一步
        
- 痛点/BUG
    
    - 在观察与数据里已经进行了叙述
        
- 改进建议
    
    - 在观察与数据里已经进行了叙述
        
- 综合评分
    
    - 基于我们需求的评分只能给5分, 6分如果算及格, 毕竟没有完成我们需要完成的任务
        

## 测试用例 -- 在arxiv.org上进行文章信息搜集

- 场景描述
    
    - 在arxiv.org上对指定关键词在指定时间段进行搜索, 对搜索结果进行搜集, 之所以做这个测试是因为google scholar的反爬做的比arxiv更严格, 所以我们也尝试了一下反爬更松的arxiv是什么情况
        
- 测试步骤
    
    - /fellou 要求fellou执行以下prompt, 帮我从arxiv.org上发现标题内容包含time series forecasting的文章, 2024年发布的, 给出这些文章的标题, 作者, 链接, Abstract, 并且把Abstract翻译成中文, 对这些文章进行深入分析, 对他们使用的方法, 适用的数据集进行分析和展示, 符合相关条件的文章有368篇, 请对其中至少30篇进行上述处理
        
- 观察与数据
    
    - 同前一个测试用例, 可以生成报告 https://chat.fellou.ai/report/0f775f71-d988-4d4f-aae5-7acff98d33d7
        
    - 报告里的三篇论文都是真实存在并且符合要求的
        
    - 明确要求了至少看要给其中的30篇的信息, 结果没有能够跟随要求, 只提供了三篇, 实际上我们还做了另一个测试, 就是不要求篇数, 结果也是就采集了3篇
        
- 优势亮点
    
- 痛点/BUG
    
    - 除了上一个用例的问题, 我们在这里还遇到过另一个问题, 就是报告会有生成了打不开的情况, 同时我们也观察到报告的生成时间有时候很长, 是不是可以用诸如md结构生成至少能保证可以打开的内容, 并且生成开销也小
        
- 改进建议
    
    - 同时生成一份md结构的报告, 或者做成默认生成现在这个web前端页面类型的报告, 同时附加一个生成md报告的选项
        
- 综合评分
    
    - 虽然没有按照指令要求完成指定数量的文章信息采集, 但至少文章内容不是幻觉, 给到6分及格分
        

  

## 测试用例 -- 在arxiv.org指定板块进行当日文章信息搜集 -- 第一次

- 场景描述
    
    - 在arxiv.org的指定板块上对当日文章信息进行搜索, 之所以做这个测试是因为上一个测试只获取了3个文章的结果, 我们在考虑是不是进一步降低Fellou和网站的交互难度, 看看是否有改进
        
- 测试步骤
    
    - /fellou 要求fellou执行以下prompt, 帮我浏览一下arxiv的computer vision and pattern recognition整理今天发布的前五十篇文章的标题, 作者, 作者院校, 文章摘要, 以及文章的结论
        
- 观察与数据
    
    - 同前一个测试用例, 可以生成报告 (系统可能有bug, 在昨晚这个测试以后, 又在同一个对话里提了其他要求, 对应报告在fellou系统上就看不到了 ... )
        
    - 同前一个测试用例, 依然只采集了三篇 ...
        
- 优势亮点
    
- 痛点/BUG
    
    - 那五十篇文章就在arxiv指定板块的页面里(https://arxiv.org/list/cs.CV/recent), 如果成功打开了那个页面, 不应该是这个结果
        
- 改进建议
    
- 综合评分
    
    - 虽然没有按照指令要求完成指定数量的文章信息采集, 但至少文章内容不是幻觉, 给到6分及格分
        

  

## 测试用例 -- 在arxiv.org指定板块进行当日文章信息搜集 -- 第二次

- 场景描述
    
    - 在arxiv.org的指定板块上对当日文章信息进行搜索, 之所以做这个测试是因为上一个测试只获取了3个文章的结果, 我们在考虑是不是进一步降低Fellou和网站的交互难度, 看看是否有改进, 做第二次的原因主要目的是想观察可重复性
        
- 测试步骤
    
    - /fellou 要求fellou执行以下prompt, 帮我浏览一下arxiv的computer vision and pattern recognition整理今天发布的前五十篇文章的标题, 作者, 作者院校, 文章摘要, 以及文章的结论
        
- 观察与数据
    
    - 同前一个测试用例, 可以生成报告
        
    - 本次采集了五十篇, 这是生成的报告链接, https://chat.fellou.ai/report/f0ffce39-a0f9-49c3-aa14-b45e42edfe1a
        
    - 本次采集开始出现幻觉 ... 前几篇文章还行, 往后就开始出现一些看似存在(arxiv的编号存在), 但是文章标题不符的结果 ...
        
- 优势亮点
    
- 痛点/BUG
    
    - 采集的内容有幻觉
        
- 改进建议
    
- 综合评分
    
    - 考虑到幻觉的存在, 给5分, 不及格
        

## 测试用例 -- 在arxiv.org指定板块进行当日文章信息搜集 -- 第三次

- 场景描述
    
    - 做第三次测试的原因, 是想通过给到准确的, 能够获取文章列表的链接的情况下(进一步降低工作难度), 看看能得到什么结果
        
- 测试步骤
    
    - /fellou 要求fellou执行以下prompt, 帮我浏览一下arxiv的computer vision and pattern recognition整理今天发布的前五十篇文章(可以从"https://arxiv.org/list/cs.CV/recent"获取)的标题, 作者, 作者院校, 文章摘要, 以及文章的结论
        
- 观察与数据
    
    - 同前一个测试用例, 可以生成报告
        
    - 本次采集了十五篇, 这是生成的报告链接, https://chat.fellou.ai/report/002ca222-562c-4712-8fde-82f217615942
        
    - 本次采集开始出现幻觉 ... 展示的内容虽然都是存在的文章, 但是只有一篇来自前述提供的链接里的当日最新, 剩下的文章既不是arxiv的recent文章, 也不是cs.CV这个板块下的文章, 不知道系统采集自何处
        
- 优势亮点
    
- 痛点/BUG
    
    - 采集的内容有幻觉
        
- 改进建议
    
- 综合评分
    
    - 考虑到幻觉的存在, 给5分, 不及格
        
    
      
    

## 测试用例 -- 日常个人消费决策信息采集

- 场景描述
    
    - 尝试了一下日常个人消费决策需要的信息采集过程
        
- 测试步骤
    
    - /fellou 要求fellou执行以下prompt, 做一下衣物毛球修剪器调研, 帮我做采购决策, 我对价格不太敏感
        
- 观察与数据
    
    - 生成了报告, 并且进行了发布 https://chat.fellou.ai/report/8952e2b2-e6ba-4b27-9bf4-d53bfa5e901f
        
    - 报告内容其实整体看下来还不错, 少了一个典型品牌松下, 其他品牌基本都覆盖了
        
    - 给出的型号和价格基本真实
        
    - 品牌虽然比较全, 但是型号不是很全面
        
- 优势亮点
    
    - 信息比较完成, 比较维度比较丰富, 购买建议方面也给了多个不同购买决策侧重点下的选择
        
- 痛点/BUG
    
    - 报告本身有bug, "功能与性能"板块打不开
        
- 改进建议
    
    - 产品最好有电商平台本身的链接, 还有相关信息最好能直接附带信息源, 以给用户信心
        
- 综合评分
    
    - 比较好的完成了任务, 可以给到8 - 9分