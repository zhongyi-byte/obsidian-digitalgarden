---
{"date":"2023-12-31","tags":["area/ai/rag"],"dg-publish":true,"dg-path":"RAG技术.md","permalink":"/RAG技术/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-31T13:56:42.495+08:00","updated":"2025-01-21T00:10:48.197+08:00"}
---

## 什么是RAG
### RAG解决什么问题
如何让大模型回答训练数据之外的知识?
1. finetuning。成本过高，每次引入新数据都需要重新训练一遍模型。
2. rag。通过引入外部知识库的方式，让大模型现场提取信息。

流程：
1. 选择外部知识库数据
2. 对外部知识库进行embedding向量化
3. 存入数据库
4. 搜索，将query转化为vecter，通过搜索引擎or向量数据库找出相近的向量，再通过大模型进行回答。
好处：能够引用真实的数据内容，提高了可靠性。



使用 LLM 的三种方式：Prompting, RAG, Fine-Tuning: RAG 用于扩展知识库，微调更多是关于改变结构（行为）而非知识。
![Pasted image 20231231202509.png](/img/user/publish/attachments/Pasted%20image%2020231231202509.png)


### RAG的组成部分
1. 语言模型
2. 外部知识模型
3. 当前场景下所需要的外部数据

## RAG评估系统
#### 可验证性（verifibality）
1. 流畅性
2. 实用性
3. 引用召回率
4. 引用精度
1和2是基本条件
3和4是互斥关系，不可能都达到100%




## devv.ai的实践
1. 评测集。
2. 自动化评测框架。可用于快速验证prompt改动造成的影响，进行a/b测试

### 开源rag框架
1. embedchain



參考資料：
1. devv.ai，一个利用rag技术实现的程序员搜索引擎，创始人@jiayuan的推特。
 * https://twitter.com/Tisoga/status/1731478506465636749
 * https://twitter.com/tisoga/status/1736544319199478175
