# awesome-TODO
我后续想精读的一些论文

# 1.Text-to-Clip Video Retrieval with Early Fusion and Re-Captioning
## 这篇就是用caption作为auxiliary task@video moment retrieval的～

# 2.MAN: Moment Alignment Network for Natural Language Moment Retrieval via Iterative Graph Adjustment
这里就是dynamic filter@卷积

# 3.Span-based Localizating Network for Natural Language Video Localization@@@思路创新
Untrimmed video+text query: NLVL(natural language video localization)
## Motivation：
1.existing solutions formulate NLVL @ranking task/multimodal matching architecture/regression task～（directly regress the video span）

2.我们就是单纯将这个task当作span-based QA的问题（）

3.**很值得学习的话术: We address NLVL task with a span-based QA approach by treating the input video as text passage, @Video Span Localization Network(on top of the standard span-based QA framework)**

4.The proposed VLSNet tackles the differences between NLVL and span-based QA through a simple and yet effective query-guided highlighting strategy(QGH). The QGH guides VSLNet to search for matching video span within a highlighted region~

# 4.Relational Recurrent Neural Networks@Relational Memory Core（可以做做实验，测试一下）
1.就是现有的memory network并不确定到底能不能解决好perform complex relational reasoning within the information they remember(**tasks involving relational reasoning**)

2.我们这里就是证明我们的intuition(confirm our intuitions that standard memory architectures may struggle at these tasks).

3.**we then improve upon these deficits by using a new memory module@(Relational Memory Core-RMC)**使用multi-head dot product attention@允许记忆可以交互interact～

## Introduction claim的观点
1.We propose that it is fruitful to consider **memory interactions** along with storage and retrieval. 虽然现有的模型可以学习compartmentalize and related distributed, vectorized memories, **they are not biased towards doing so explicitly**~

2.我们就是hypothesize这个bias可能能够帮助模型更好理解how memories are related，因此可能give it a better capacity for relational reasoning over time.

### 关于关系推理的理解
关系推理在作者看来是一个process of understanding the ways in which entites are connected and using this understanding to 完成some higher order goal～

One can imagine a spectrum of neural network inductive biases that can be cast in the language of relational reasoning~

1.convolutional kernel@计算pixels之间的relation(linear combination within a receptive field~)

2.一些previous方法使得relational inductive bias more explicit: message passing neural networks/Relation Network/

3.even further，some approaches emphasize that more capable reasoning may be possible by employing simple computational principles~(更加有能力的推理可能通过一些简单的计算原理实现～)

4.一些relations可能在space 不是be tied to proximity in space的，non-local计算可能很适合@far away～

5.对于temporal，很多关于attention的工作～

6.Memory Network+LSTM～

![](RelationMem.jpg)

### 其实就是对RNNcell的一个改进～

# 5.VLANet: Video-Language Alignment Network for Weakly-Supervised Video Moment Retrieval@借鉴了对比学习Contrasive Loss
localize the temporal momemht in untrimmed video@NL query. 

## Motivation
1.目前关于VMR这个任务，很多有监督学习的方法已经被提出了。

# 6.Weakly supervised Video Moment Retrieval From Text Queries@weakly的一种方法辣～TODO
## Motivation
1.Propose a joint visual-semantic embedding based framework@(only video-level sentence descriptions~)

2.utilize latent alignment between video frames and sentence descriptions using Text-Guided Attention(TGA).

# 7.Visual Relationship Detection with Deep Structural Ranking@AAAI 2018
VRD任务，关于咱们的Visual Relationship 就是指形如<object1,predicate,object2>的关系三元组，于是Visual Relationship Detection就是VRD任务包括:

1)检测和定位图上地多对object；

2)然后对每一对object的交互关系(predicate)进行分类

## 任务的主要难点就是:
1.relationship是object与predicate的组合(注意)，因此其语义空间要比object或者predicate的要大许多～紧接着而来的就是训练数据的问题，穷尽所有relationship总是很困难的。因此，如何从少量
的样本中进行relationship的有效学习就显得尤为关键～

## Motivation:
1.Visual Relationship detection旨在describe the interactions between pair of objects，可是事实上不同于individual object learning tasks，这个任务很难仅仅利用visual appearance of objects来识别/。

2.limited human effort，所以annotations for visual relationships@经常是incomplete@model训练～

## 我们的工作
1.我们提出了一个framework@**Deep Structural Ranking**

![](DeepRank.jpg)

# 8.On exploring Undetermined Relationships for Visual Relationship Detection


# 9.Visual Relationship Detection with Relative Location Mining

# 10.DGCN: Dynamic Graph Convolutional Network for Efficient Multi-Person Pose Estimation

# 11.Explanation-based Weakly-supervised Learning of Visual Relations with Graph Networks

# 12.Hierarchical Feature-Pair Relation Networks for Face Recognition

# 13.Spatial-aware Graph Relation Network for Large-Scale Object Detection

# 14.Exploring COntext and Visual Pattern of Relationship for Scene Graph Generation

# 15.Attentive Relational Networks for Mapping Images to Scene Graphs

# 16.ORD: Object Relationship Discovery for Visual Dialogue Generation@@这里就是对于VQA而言将关系建立的很好，我们用一个层次的方式来进行encoding
第一个stage就是local的object结合relation的aggregation，然后就是object-object interaction～

# 17.Spatio-Temporal Dynamics and Semantic Attribute Enriched Visual Encoding for Video Captioning

# 18.Spatio-temporal Relational Reasoning for Video QA

# 19.Learning Spatio-temporal Representation with Local and Global Diffusion

# 20.Reinforced Mnemonic Reader for MRC

# 21.Explicit Utilization of General Knowledge in Machine Reading Comprehension

# 22.FusionNet:Fusing via Fully-aware Attention with Application to Machine Comprehension

# 23.Stochastic Answer Networks for MRC

# 24.QANet: Combining Local Convolution with Global Self-attention for MRC

# 25.Gated Self-Matching Networks for Reading Comprehension and Question ANswering

# 26.Machine Reading Comprehension Using Structural Knowledge Graph-aware Network

# 27.Exploring Graph-Structured Passage Representation for Multi-hop Reading Comprehension with GNN

# 28.Generating Multi-hop Reasoning Questions to Improve Machine Reading Comprehension@key

# 29.GraphFlow: Exploiting Conversation Flow with GNN for Conversational Machine Comprehension

# 30.Learning Cross-Modal Context Graph for Visual Grounding@AAAI2020

# 31.Knowledge-Based Video Question Answering with Unsupervised Scene Descriptions

# 32.Dynamic Graph Representation Learning for Video Dialog via Multi-Modal Shuffled Transformers@AAAI2021

# 33.Spatiotemporal Graph NN based Mask Reconstruction for Video Object Segmentation@AAAI 2021

# 34.Video-Grounded Dialogues with Pretrained Generation Language Models

# 35.Multimodal Transformer Networks for End-to-End Video-Grounded Dialogue Systems

# 36.Learning Action Primitives for Multi-level Video Event Understanding

# 37.A Deep Reinforcement Learning Based Multi-step Coarse to Fine Question Answering System(MSCQA)

# 38.Span-Selection Pretraining for QA@2020 ACL

# 39.Stacking With Auxiliary Features for Visual QA@2018ACL

# 40.Coarse-to-Fine Pretraining for Named Entity Recognition@2020 ACL

# 41.Evidence Sentence Extraction for MRC

# 42.Coarse-to-Fine Question Answering for Long Documents

# 43.Coarse-Grain Fine-Grain Coattention Network for Multi-evidence QA@ICLR 2019

# 44.Non-Autoregressive Coarse-to_Fine Video Captioning

# 45.Fully Convolutional Video Captioning with Coarse-to-Fine and Inherited Attention@AAAI2019

# 46.A Graph-based Relevance Matching Model for Ad-hoc Retrieval@必看

# 47.Improving Span-based QA systems with Coarsely Labeled Data.@必看

# 48.























