


<p> 
<a href="https://github.com/liguodongiot/llm-action/stargazers">
<img src="https://img.shields.io/github/stars/liguodongiot/llm-action?style=social" > </a>
<a href="https://github.com/liguodongiot/llm-action/blob/main/pic/wx.jpg"> <img src="https://img.shields.io/badge/吃果冻不吐果冻皮-1AAD19.svg?style=plastic&logo=wechat&logoColor=white" > </a>
<a href="https://www.zhihu.com/people/liguodong-iot"> <img src="https://img.shields.io/badge/吃果冻不吐果冻皮-0079FF.svg?style=plastic&logo=zhihu&logoColor=white"> </a>
<a href="https://juejin.cn/user/3642056016410728"> <img src="https://img.shields.io/badge/掘金-吃果冻不吐果冻皮-000099.svg?style=plastic&logo=juejin"> </a>
<a href="https://liguodong.blog.csdn.net/"> <img src="https://img.shields.io/badge/CSDN-吃果冻不吐果冻皮-6B238E.svg"> </a>
</p> 


## 目录

- 🔥 [LLM训练](#llm训练)
  - 🐫 [LLM训练实战](#llm训练实战)
  - 🐼 [LLM参数高效微调技术原理综述](#llm微调技术原理)
  - 🐰 [LLM参数高效微调技术实战](#llm微调实战)
  - 🐘 [LLM分布式训练并行技术](#llm分布式训练并行技术)
  - 🌋 [分布式AI框架](#分布式ai框架)
  - 📡 [分布式训练网络通信](#分布式训练网络通信)
- 🐎 [LLM推理](#llm推理)
  - 🚀 [LLM推理框架](#llm推理框架)
  - ✈️ [LLM推理优化技术](#llm推理优化技术)
- ♻️ [LLM压缩](#llm压缩)
  - 📐 [LLM量化](#llm量化)
  - 🔰 [LLM剪枝](#llm剪枝)
  - 💹 [LLM知识蒸馏](#llm知识蒸馏)
  - ♑️ [低秩分解](#低秩分解)
- ♍️ [LLM算法架构](#llm算法架构)
- :jigsaw: [LLM应用开发](#llm应用开发)
- 🀄️ [LLM国产化适配](#llm国产化适配)
- 🔯 [AI编译器](#ai编译器)
- 🔘 [AI基础设施](#ai基础设施)
- 💟 [LLMOps](#llmops)
- 🍄 [LLM生态相关技术](#llm生态相关技术)
- 🔨 [服务器基础环境安装及常用工具](#服务器基础环境安装及常用工具)
- 💬 [LLM学习交流群](#llm学习交流群)
- 👥 [微信公众号](#微信公众号)
- ⭐️ [Star History](#star-history)

## LLM训练


### [LLM分布式训练并行技术](https://github.com/liguodongiot/llm-action/tree/main/docs/llm-base/distribution-parallelism)

近年来，随着Transformer、MOE架构的提出，使得深度学习模型轻松突破上万亿规模参数，传统的单机单卡模式已经无法满足超大模型进行训练的要求。因此，我们需要基于单机多卡、甚至是多机多卡进行分布式大模型的训练。

而利用AI集群，使深度学习算法更好地从大量数据中高效地训练出性能优良的大模型是分布式机器学习的首要目标。为了实现该目标，一般需要根据硬件资源与数据/模型规模的匹配情况，考虑对计算任务、训练数据和模型进行划分，从而进行分布式训练。因此，分布式训练相关技术值得我们进行深入分析其背后的机理。

下面主要对大模型进行分布式训练的并行技术进行讲解，本系列大体分九篇文章进行讲解。

- [大模型分布式训练并行技术（一）-概述](https://zhuanlan.zhihu.com/p/598714869)
- [大模型分布式训练并行技术（二）-数据并行](https://zhuanlan.zhihu.com/p/650002268)
- [大模型分布式训练并行技术（三）-流水线并行](https://zhuanlan.zhihu.com/p/653860567)
- [大模型分布式训练并行技术（四）-张量并行](https://zhuanlan.zhihu.com/p/657921100)
- [大模型分布式训练并行技术（五）-序列并行](https://zhuanlan.zhihu.com/p/659792351)
- [大模型分布式训练并行技术（六）-多维混合并行](https://zhuanlan.zhihu.com/p/661279318)
- [大模型分布式训练并行技术（七）-自动并行](https://zhuanlan.zhihu.com/p/662517647)
- [大模型分布式训练并行技术（八）-MOE并行](https://zhuanlan.zhihu.com/p/662518387)
- [大模型分布式训练并行技术（九）-总结](https://zhuanlan.zhihu.com/p/667051845)


### 实战3：transformer模型构建实训

本实训课程主要培养学生的模型训练能力，主要使用6B到65B的多个模型，从全量微调到高效微调（LoRA，QLoRA，P-Tuning v2），再到RLHF（基于人工反馈的强化学习）。

| LLM                         | 预训练/SFT/RLHF...            | 参数     | 教程                                                                                                                                                                                                                     | 代码                                                                                     |
| --------------------------- | ----------------------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------- |
| Alpaca                      | full fine-turning             | 7B       | [从0到1复现斯坦福羊驼（Stanford Alpaca 7B）](https://zhuanlan.zhihu.com/p/618321077)                                                                                                                                        | [配套代码](https://github.com/liguodongiot/llm-action/tree/main/train/alpaca)               |
| Alpaca(LLaMA)               | LoRA                          | 7B~65B   | 1.[足够惊艳，使用Alpaca-Lora基于LLaMA(7B)二十分钟完成微调，效果比肩斯坦福羊驼](https://zhuanlan.zhihu.com/p/619426866)<br>2. [使用 LoRA 技术对 LLaMA 65B 大模型进行微调及推理](https://zhuanlan.zhihu.com/p/632492604)    | [配套代码](https://github.com/liguodongiot/llm-action/tree/main/train/alpaca-lora)          |
| BELLE(LLaMA/Bloom)          | full fine-turning             | 7B       | 1.[基于LLaMA-7B/Bloomz-7B1-mt复现开源中文对话大模型BELLE及GPTQ量化](https://zhuanlan.zhihu.com/p/618876472) <br> 2. [BELLE(LLaMA-7B/Bloomz-7B1-mt)大模型使用GPTQ量化后推理性能测试](https://zhuanlan.zhihu.com/p/621128368) | N/A                                                                                      |
| ChatGLM                     | LoRA                          | 6B       | [从0到1基于ChatGLM-6B使用LoRA进行参数高效微调](https://zhuanlan.zhihu.com/p/621793987)                                                                                                                                      | [配套代码](https://github.com/liguodongiot/llm-action/tree/main/train/chatglm-lora)         |
| ChatGLM                     | full fine-turning/P-Tuning v2 | 6B       | [使用DeepSpeed/P-Tuning v2对ChatGLM-6B进行微调](https://zhuanlan.zhihu.com/p/622351059)                                                                                                                                     | [配套代码](https://github.com/liguodongiot/llm-action/tree/main/train/chatglm)              |
| Vicuna(LLaMA)               | full fine-turning             | 7B       | [Vicuna训练实战](https://zhuanlan.zhihu.com/p/624012908)                                                                                                                            | N/A                                                                                      |
| OPT                         | RLHF                          | 0.1B~66B | 1.[使用RLHF训练DeepSpeed Chat](https://zhuanlan.zhihu.com/p/626159553) <br> 2. [一键式 RLHF 训练 DeepSpeed Chat（二）：实践篇](https://zhuanlan.zhihu.com/p/626214655)                                 | [配套代码](https://github.com/liguodongiot/llm-action/tree/main/train/deepspeedchat)        |
| Chinese-LLaMA-Alpaca(LLaMA) | LoRA（预训练+微调）           | 7B       | [Alpaca模型词表扩充和预训练](https://zhuanlan.zhihu.com/p/631360711)                                                                                                                            | [配套代码](https://github.com/liguodongiot/llm-action/tree/main/train/chinese-llama-alpaca) |
| LLaMA                       | QLoRA                         | 7B/65B   | [高效微调技术QLoRA实战](https://zhuanlan.zhihu.com/p/636644164)                                                                                                                         | [配套代码](https://github.com/liguodongiot/llm-action/tree/main/train/qlora)                |


### 课程4：大模型的优化与微调

对于普通大众来说，进行大模型的预训练或者全量微调遥不可及。由此，催生了各种参数高效微调技术，让科研人员或者普通开发者有机会尝试微调大模型。

因此，该技术值得我们进行深入分析其背后的机理，本课程共包含7个部分，24个课时。

- [大语言模型的参数微调（一）-背景、参数高效微调简介](https://zhuanlan.zhihu.com/p/635152813)
- [大语言模型的参数微调（二）-BitFit、Prefix Tuning、Prompt Tuning](https://zhuanlan.zhihu.com/p/635686756)
- [大语言模型的参数微调（三）-P-Tuning、P-Tuning v2](https://zhuanlan.zhihu.com/p/635848732)
- [大语言模型的参数微调（四）-Adapter Tuning及其变体](https://zhuanlan.zhihu.com/p/636038478)
- [大语言模型的参数微调（五）-LoRA、AdaLoRA、QLoRA](https://zhuanlan.zhihu.com/p/636215898)
- [大语言模型的参数微调（六）-MAM Adapter、UniPELT](https://zhuanlan.zhihu.com/p/636362246)
- [大语言模型的参数微调（七）-最佳实践、总结](https://zhuanlan.zhihu.com/p/649755252)

### 实战4：模型优化微调实训

**大语言模型的参数微调实战**，本实训课主要针对 HuggingFace PEFT 框架支持的一些高效微调技术进行讲解。

| 实训内容                                                                                                | 代码                                                                                                      | 框架             |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | ---------------- |
| [大语言模型的参数微调实战（一）-PEFT环境搭建](https://zhuanlan.zhihu.com/p/651744834)          | N/A                                                                                                       | HuggingFace PEFT |
| [大语言模型的参数微调实战（二）-Prompt Tuning](https://zhuanlan.zhihu.com/p/646748939)               | [配套代码](https://github.com/liguodongiot/llm-action/blob/main/train/peft/clm/peft_prompt_tuning_clm.ipynb) | HuggingFace PEFT |
| [大语言模型的参数微调实战（三）-P-Tuning](https://zhuanlan.zhihu.com/p/646876256)                    | [配套代码](https://github.com/liguodongiot/llm-action/blob/main/train/peft/clm/peft_p_tuning_clm.ipynb)      | HuggingFace PEFT |
| [大语言模型的参数微调实战（四）-Prefix Tuning / P-Tuning v2](https://zhuanlan.zhihu.com/p/648156780) | [配套代码](https://github.com/liguodongiot/llm-action/blob/main/train/peft/clm/peft_p_tuning_v2_clm.ipynb)   | HuggingFace PEFT |
| [大语言模型的参数微调实战（五）-LoRA](https://zhuanlan.zhihu.com/p/649315197)                        | [配套代码](https://github.com/liguodongiot/llm-action/blob/main/train/peft/clm/peft_lora_clm.ipynb)          | HuggingFace PEFT |
| [大语言模型的参数微调实战（六）-IA3](https://zhuanlan.zhihu.com/p/649707359)                         | [配套代码](https://github.com/liguodongiot/llm-action/blob/main/train/peft/clm/peft_ia3_clm.ipynb)           | HuggingFace PEFT |
| [大语言模型的参数微调实战（七）-基于LoRA微调多模态大模型](https://zhuanlan.zhihu.com/p/670048482)       |     [配套代码](https://github.com/liguodongiot/llm-action/blob/main/train/peft/multimodal/blip2_lora_int8_fine_tune.py) | HuggingFace PEFT |
| [大语言模型的参数微调实战（八）-使用INT8/FP4/NF4微调大模型](https://zhuanlan.zhihu.com/p/670116171)    |     [配套代码](https://github.com/liguodongiot/llm-action/blob/main/train/peft/multimodal/finetune_bloom_bnb_peft.ipynb) | PEFT、bitsandbytes |







### 分布式AI框架

- [PyTorch](https://github.com/liguodongiot/llm-action/tree/main/train/pytorch/)
  - PyTorch 单机多卡训练
  - PyTorch 多机多卡训练
- [Megatron-LM](https://github.com/liguodongiot/llm-action/tree/main/train/megatron)
  - Megatron-LM 单机多卡训练
  - Megatron-LM 多机多卡训练
  - [基于Megatron-LM从0到1完成GPT2模型预训练、模型评估及推理](https://juejin.cn/post/7259682893648724029)
- [DeepSpeed](https://github.com/liguodongiot/llm-action/tree/main/train/deepspeed)
  - DeepSpeed 单机多卡训练
  - DeepSpeed 多机多卡训练
- [Megatron-DeepSpeed](https://github.com/liguodongiot/llm-action/tree/main/train/megatron-deepspeed)
  - 基于 Megatron-DeepSpeed 从 0 到1 完成 LLaMA 预训练
  - 基于 Megatron-DeepSpeed 从 0 到1 完成 Bloom 预训练


### 分布式训练网络通信

待更新...


**[⬆ 一键返回目录](#目录)**

## [LLM推理](https://github.com/liguodongiot/llm-action/tree/main/inference)

### LLM推理框架

- [大模型推理框架概述](https://www.zhihu.com/question/625415776/answer/3243562246)
- [大模型的好伙伴，浅析推理加速引擎FasterTransformer](https://zhuanlan.zhihu.com/p/626008090)
- [模型推理服务化框架Triton保姆式教程（一）：快速入门](https://zhuanlan.zhihu.com/p/629336492)
- [模型推理服务化框架Triton保姆式教程（二）：架构解析](https://zhuanlan.zhihu.com/p/634143650)
- [模型推理服务化框架Triton保姆式教程（三）：开发实践](https://zhuanlan.zhihu.com/p/634444666)
- [TensorRT-LLM保姆级教程（一）-快速入门](https://zhuanlan.zhihu.com/p/666849728)
- [TensorRT-LLM保姆级教程（二）-开发实践](https://zhuanlan.zhihu.com/p/667572720)
- TensorRT-LLM保姆级教程（三）-基于Triton完成模型服务化
- TensorRT-LLM保姆级教程（四）-新模型适配
- TensorRT



### LLM推理优化技术

- [LLM推理优化技术概述]()
- PageAttention
- FlashAttention

## LLM压缩

近年来，随着Transformer、MOE架构的提出，使得深度学习模型轻松突破上万亿规模参数，从而导致模型变得越来越大，因此，我们需要一些大模型压缩技术来降低模型部署的成本，并提升模型的推理性能。
模型压缩主要分为如下几类：

-   剪枝（Pruning）
-   知识蒸馏（Knowledge Distillation）
-   量化



### [LLM量化](https://github.com/liguodongiot/llm-action/tree/main/model-compression/quantization)

本系列将针对一些常见大模型量化方案（GPTQ、LLM.int8()、SmoothQuant、AWQ等）进行讲述。

- [大模型量化概述](https://www.zhihu.com/question/627484732/answer/3261671478)
- 量化感知训练：
    - [大模型量化感知训练技术原理：LLM-QAT](https://zhuanlan.zhihu.com/p/647589650)
    - [大模型量化感知微调技术原理：QLoRA]()
    - PEQA
- 训练后量化：
    - [大模型量化技术原理：GPTQ、LLM.int8()](https://zhuanlan.zhihu.com/p/680212402)
    - [大模型量化技术原理：SmoothQuant](https://www.zhihu.com/question/576376372/answer/3388402085)
    - [大模型量化技术原理：AWQ、AutoAWQ](https://zhuanlan.zhihu.com/p/681578090)
    - [大模型量化技术原理：SpQR](https://zhuanlan.zhihu.com/p/682871823)
    - [大模型量化技术原理：ZeroQuant系列](https://zhuanlan.zhihu.com/p/683813769)
- [大模型量化技术原理：总结]()


### LLM剪枝


**结构化剪枝**：

- LLM-Pruner

**非结构化剪枝**：

- SparseGPT
- LoRAPrune
- Wanda

### LLM知识蒸馏

- [大模型知识蒸馏概述](https://www.zhihu.com/question/625415893/answer/3243565375)

**Standard KD**:

使学生模型学习教师模型(LLM)所拥有的常见知识，如输出分布和特征信息，这种方法类似于传统的KD。

- MINILLM
- GKD

**EA-based KD**:

不仅仅是将LLM的常见知识转移到学生模型中，还涵盖了蒸馏它们独特的涌现能力。具体来说，EA-based KD又分为了上下文学习（ICL）、思维链（CoT）和指令跟随（IF）。

In-Context Learning：

- In-Context Learning distillation

Chain-of-Thought：

- MT-COT
- Fine-tune-CoT
- DISCO
- SCOTT
- SOCRATIC CoT

Instruction Following：

- Lion

### 低秩分解

低秩分解旨在通过将给定的权重矩阵分解成两个或多个较小维度的矩阵，从而对其进行近似。低秩分解背后的核心思想是找到一个大的权重矩阵W的分解，得到两个矩阵U和V，使得W≈U V，其中U是一个m×k矩阵，V是一个k×n矩阵，其中k远小于m和n。U和V的乘积近似于原始的权重矩阵，从而大幅减少了参数数量和计算开销。

在LLM研究的模型压缩领域，研究人员通常将多种技术与低秩分解相结合，包括修剪、量化等。

- ZeroQuant-FP（低秩分解+量化）
- LoRAPrune（低秩分解+剪枝）

## [LLM算法架构](https://github.com/liguodongiot/llm-action/tree/main/docs/llm-base/ai-algo)

- [大模型算法演进](https://zhuanlan.zhihu.com/p/600016134)
- ChatGLM / ChatGLM2 / ChatGLM3 大模型解析
- Bloom 大模型解析
- LLaMA / LLaMA2 大模型解析
- [百川智能开源大模型baichuan-7B技术剖析](https://www.zhihu.com/question/606757218/answer/3075464500)
- [百川智能开源大模型baichuan-13B技术剖析](https://www.zhihu.com/question/611507751/answer/3114988669)


## LLM应用开发

大模型是基座，要想让其变成一款产品，我们还需要一些其他相关的技术，比如：向量数据库（Pinecone、Milvus、Vespa、Weaviate），LangChain等。

- [云原生向量数据库Milvus（一）-简述、系统架构及应用场景](https://zhuanlan.zhihu.com/p/476025527)
- [云原生向量数据库Milvus（二）-数据与索引的处理流程、索引类型及Schema](https://zhuanlan.zhihu.com/p/477231485)
- [关于大模型驱动的AI智能体Agent的一些思考](https://zhuanlan.zhihu.com/p/651921120)



## [LLM国产化适配](https://github.com/liguodongiot/llm-action/tree/main/docs/llm_localization)

随着 ChatGPT 的现象级走红，引领了AI大模型时代的变革，从而导致 AI 算力日益紧缺。与此同时，中美贸易战以及美国对华进行AI芯片相关的制裁导致 AI 算力的国产化适配势在必行。本系列将对一些国产化 AI 加速卡进行讲解。

- [大模型国产化适配1-华为昇腾AI全栈软硬件平台总结](https://zhuanlan.zhihu.com/p/637918406)
- [大模型国产化适配2-基于昇腾910使用ChatGLM-6B进行模型推理](https://zhuanlan.zhihu.com/p/650730807)
- [大模型国产化适配3-基于昇腾910使用ChatGLM-6B进行模型训练](https://zhuanlan.zhihu.com/p/651324599)
- [大模型国产化适配4-基于昇腾910使用LLaMA-13B进行多机多卡训练](https://zhuanlan.zhihu.com/p/655902796)
- [大模型国产化适配5-百度飞浆PaddleNLP大语言模型工具链总结](https://juejin.cn/post/7291513759470960679)
- [大模型国产化适配6-基于昇腾910B快速验证ChatGLM3-6B/BaiChuan2-7B模型推理](https://zhuanlan.zhihu.com/p/677799157)



**[⬆ 一键返回目录](#目录)**


## [AI编译器](https://github.com/liguodongiot/llm-action/tree/main/ai-compiler)

AI编译器是指将机器学习算法从开发阶段，通过变换和优化算法，使其变成部署状态。

- [AI编译器技术剖析（一）-概述](https://zhuanlan.zhihu.com/p/669347560)
- [AI编译器技术剖析（二）-传统编译器](https://zhuanlan.zhihu.com/p/671477784)
- [AI编译器技术剖析（三）-树模型编译工具 Treelite 详解](https://zhuanlan.zhihu.com/p/676723324)
- [AI编译器技术剖析（四）-编译器前端]()
- [AI编译器技术剖析（五）-编译器后端]()
- [AI编译器技术剖析（六）-主流编译框架]()
- [AI编译器技术剖析（七）-深度学习模型编译优化]()
- [lleaves：使用 LLVM 编译梯度提升决策树将预测速度提升10+倍](https://zhuanlan.zhihu.com/p/672584013)

框架：

- MLIR
- XLA
- TVM




## AI基础设施

- [AI 集群基础设施 NVMe SSD 详解](https://juejin.cn/post/7311604023184162835)
- [AI 集群基础设施 InfiniBand 详解](https://zhuanlan.zhihu.com/p/673903240)
- [大模型训练基础设施：算力篇]()


### AI加速卡

- [AI芯片技术原理剖析（一）：国内外AI芯片概述](https://zhuanlan.zhihu.com/p/667686665)
- AI芯片技术原理剖析（二）：英伟达GPU 
- AI芯片技术原理剖析（三）：谷歌TPU

### AI集群

待更新...


### [AI集群网络通信](https://github.com/liguodongiot/llm-action/tree/main/docs/llm-base/network-communication)

待更新...

- 分布式训练网络通讯原语
- AI 集群通信软硬件


## LLMOps

- [在 Kubernetes 上部署机器学习模型的指南](https://zhuanlan.zhihu.com/p/676389726)
- [使用 Kubernetes 部署机器学习模型的优势](https://juejin.cn/post/7320513026188099619)



## LLM生态相关技术

- [大模型词表扩充必备工具SentencePiece](https://zhuanlan.zhihu.com/p/630696264)
- [大模型实践总结](https://www.zhihu.com/question/601594836/answer/3032763174)
- [ChatGLM 和 ChatGPT 的技术区别在哪里？](https://www.zhihu.com/question/604393963/answer/3061358152)
- [现在为什么那么多人以清华大学的ChatGLM-6B为基座进行试验？](https://www.zhihu.com/question/602504880/answer/3041965998)
- [为什么很多新发布的大模型默认使用BF16而不是FP16？](https://www.zhihu.com/question/616600181/answer/3195333332)
- [LESS：仅选择5%有影响力的数据优于全量数据集进行目标指令微调](https://zhuanlan.zhihu.com/p/686007325)



**[⬆ 一键返回目录](#目录)**

## 服务器基础环境安装及常用工具

基础环境安装：

- [英伟达A800加速卡常见软件包安装命令](https://github.com/liguodongiot/llm-action/blob/main/docs/llm-base/a800-env-install.md)
- [英伟达H800加速卡常见软件包安装命令](https://github.com/liguodongiot/llm-action/blob/main/docs/llm-base/h800-env-install.md)
- [昇腾910加速卡常见软件包安装命令](https://github.com/liguodongiot/llm-action/blob/main/docs/llm_localization/ascend910-env-install.md)

常用工具：

- [Linux 常见命令大全](https://juejin.cn/post/6992742028605915150)
- [Conda 常用命令大全](https://juejin.cn/post/7089093437223338015)
- [Poetry 常用命令大全](https://juejin.cn/post/6999405667261874183)
- [Docker 常用命令大全](https://juejin.cn/post/7016238524286861325)
- [Docker Dockerfile 指令大全](https://juejin.cn/post/7016595442062327844)
- [Kubernetes 常用命令大全](https://juejin.cn/post/7031201391553019911)
- [集群环境 GPU 管理和监控工具 DCGM 常用命令大全](https://github.com/liguodongiot/llm-action/blob/main/docs/llm-base/dcgmi.md)

## LLM学习交流群

我创建了大模型相关的学习交流群，供大家一起学习交流大模型相关的最新技术，目前已有5个群，每个群都有上百人的规模，**可加我微信进群**（加微信请备注来意，如：进大模型学习交流群+GitHub，进大模型推理加速交流群+GitHub、进大模型应用开发交流群+GitHub等）。**一定要备注哟，否则不予通过**。

PS：**成都有个本地大模型交流群，想进可以另外单独备注下。**

<p align="center">
  <img src="https://github.com/liguodongiot/llm-action/blob/main/pic/wx.jpg">
</p>

## 微信公众号

微信公众号：**吃果冻不吐果冻皮**，该公众号主要分享AI工程化（大模型、MLOps等）相关实践经验，免费电子书籍、论文等。

<p align="center">
  <img src="https://github.com/liguodongiot/llm-action/blob/main/pic/wx-gzh.png" >
</p>

**[⬆ 一键返回目录](#目录)**

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=liguodongiot/llm-action&type=Date)](https://star-history.com/#liguodongiot/llm-action&Date)
