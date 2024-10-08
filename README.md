# 入门向从零开始RAG+多模态大模型实战，丝滑简单
## NVIDIA AI-AGENT夏季训练营

### 项目名称：AI-AGENT夏季训练营 — 金融风控垂域RAG + 多模态大模型项目
### 报告日期：2024年8月18日
### 项目负责人：Amishor

### 项目概述：
金融行业的风险控制对于企业和机构的稳定运行至关重要。传统的风控系统在面对复杂的数据和监管要求时常常显得力不从心。为了让更多人能够轻松上手并理解先进的风控技术，本项目从零开始，通过整合监管文件和统计数据，用户能够快速理解和应用风险管理策略。系统支持文字、图像和语音输入，操作简单，适合入门用户在金融风控领域的学习与应用。

### 项目亮点:
1.RAG技术的应用: 通过检索增强生成技术，对监管文件进行高效检索，并在此基础上生成智能响应，极大提高了对法规与政策的理解和执行能力。

2.多模态问答大模型: 除了传统的文本问答，系统具备处理文字、图像和语音输入的能力，通过对图像（如统计图表）进行分析，获取详细的数据分析结果。

3.实用性与创新性: 该项目通过融合前沿的 AI 技术和金融风险管理实践，为金融机构提供了一个创新且实用的风控工具，提高决策效率和准确性。


### 模型选择
项目依托于Nvidia的NIM平台，综合采用了嵌入模型(NV-Embed-QA)和大语言模型(meta/llama-3.1-405b-instruct，microsoft/phi-3-vision-128k-instruct)来构建RAG + 多模态大模型。选择llama-3.1-405b-instruct模型的理由在于其能够高效地从大规模文本库中检索相关信息，以提供更精准和上下文相关的答案。phi-3-vision-128k-instruct的选择是为了增强系统对多种输入形式的处理能力，支持文本、图像，可以帮助用户通过图像轻松查询复杂的统计数据。

### 数据的构建
数据构建主要包括对监管文件的收集和向量化处理。采用NV-Embed-QA将文本数据转化为高维向量，使其能够在向量空间中进行高效检索。向量化处理的优势在于能够显著提升检索速度和准确性，并且在面对大规模数据时仍能保持良好的性能。

### 功能整合（进阶版RAG）
项目整合了语音生成功能，使得用户可以将RAG检索到的信息以语音形式输出。同时，通过多模态模型的集成，系统能够处理用户上传的统计数据图像，并将其转化为可分析的数据信息。

### 实施步骤
### 环境搭建
开发环境的搭建包括安装Python及相关库（包括LangChain、Torch等），配置必要的API密钥和数据存储路径。使用Anaconda进行环境隔离，确保不同项目之间的依赖库不产生冲突。

### 测试与调优
测试部分设计了多种测试用例，涵盖了监管文本文件、文本转语音、统计数据图像输入的场景。通过调优模型、增加数据量等方式，提高了系统的响应速度和准确性。

### 集成与部署
各模块的集成通过API的方式实现，最终在本地进行部署。部署过程中关注了系统的稳定性。

### 项目成果与展示
### 应用场景展示
该项目在金融风控领域的具体应用场景包监管合规性检查、数据分析支持等。系统能够快速解答用户关于监管要求的疑问，并通过图像识别技术，将上传的统计图表转化为可用的数据格式进行进一步分析。

#### 功能演示
演示包括系统的主要功能，如文本检索、多轮对话、语音输出、图像数据分析等。

### 问题与解决方案
### 问题分析
在项目实施过程中，主要遇到的问题包括数据的多样性处理难度、模型集成的复杂性以及多模态输入的响应速度。

### 解决措施
针对数据多样性的问题，采用了数据增强的策略。通过将RAG和多模态模型进行有效的集成，解决了模型集成的复杂性。

### 项目总结与展望
### 项目评估
项目整体表现良好，实现了从零开始搭建一个金融风控系统的目标。项目亮点在于其多模态处理能力和对专业文献的精准检索能力，但在处理更大规模的数据时，仍有进一步优化的空间。

### 未来方向
未来可以考虑扩展系统的应用场景，如将其应用于其他领域的风控或数据分析。同时，进一步优化多模态处理的性能和扩展系统的实时响应能力，也是未来的发展方向。
