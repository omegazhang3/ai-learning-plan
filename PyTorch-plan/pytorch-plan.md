# PyTorch 每日学习计划（1小时/天）

基于学习计划第一阶段：**PyTorch 上手**，共 30 天，每天 1 小时。
目标：熟练掌握 PyTorch，为第二阶段"从零实现 Transformer"打基础。

---

## 第 1 周：Tensor 基础与环境搭建

### Day 1 — 环境搭建 + PyTorch 安装
- [ ] 安装 PyTorch（`pip install torch torchvision torchaudio`）
- [ ] 验证 GPU 是否可用（`torch.cuda.is_available()`）
- [ ] 创建第一个 `.py` 文件，打印 PyTorch 版本
- 📖 阅读:
  - [PyTorch 安装指南](https://pytorch.org/get-started/locally/)
  - [PyTorch 官方教程首页](https://pytorch.org/tutorials/)
  - [Learn PyTorch: 00 Getting Started](https://www.learnpytorch.io/00_pytorch_fundamentals/)
- 🎬 视频:
  - [freeCodeCamp PyTorch Tutorial (前20分钟)](https://www.youtube.com/watch?v=G_RCsL7bxWg)
- 时间: 30 分钟安装 + 30 分钟熟悉官方文档首页

### Day 2 — Tensor 创建
- [ ] 学习 Tensor 创建方式：`torch.tensor()`, `torch.zeros()`, `torch.ones()`, `torch.randn()`, `torch.arange()`
- [ ] 理解 shape、dtype、device 三个核心属性
- [ ] 练习：创建不同 shape 的 tensor 并打印
- 📖 阅读:
  - [PyTorch 官方: Tensor Quickstart](https://pytorch.org/tutorials/beginner/basics/tensorqs_tutorial.html)
  - [Learn PyTorch: 00 Tensor Fundamentals](https://www.learnpytorch.io/00_pytorch_fundamentals/#introduction-to-tensors)
  - [d2l.ai: 2.1 数据操作](https://d2l.ai/chapter_preliminaries/ndarray.html)
- 🎬 视频:
  - [Karpathy: Neural Networks Zero to Hero EP1 (前30分钟)](https://www.youtube.com/watch?v=VMj-3S1tku0)
- 时间: 60 分钟

### Day 3 — Tensor 索引与切片
- [ ] 学习基本索引：`x[0]`, `x[:, 1]`, `x[1:3, :]`
- [ ] 学习布尔索引：`x[x > 0]`
- [ ] 学习 `torch.where()`, `torch.masked_select()`
- [ ] 练习：对一个 4x4 矩阵做各种切片操作
- 📖 阅读:
  - [PyTorch 官方: Tensor Indexing](https://pytorch.org/docs/stable/tensors.html)
  - [NumPy 索引（PyTorch 通用）](https://numpy.org/doc/stable/reference/arrays.indexing.html)
  - [d2l.ai: 2.1.3 索引和切片](https://d2l.ai/chapter_preliminaries/ndarray.html#indices-and-slicing)
- 🎬 视频:
  - [3Blue1Brown: Essence of Linear Algebra EP1 (向量是什么)](https://www.youtube.com/watch?v=fNk_zzaMoSs)
- 时间: 60 分钟

### Day 4 — Tensor 数学运算
- [ ] 逐元素运算：`+`, `-`, `*`, `/`, `torch.sqrt()`, `torch.exp()`
- [ ] 归约运算：`torch.sum()`, `torch.mean()`, `torch.max()`, `torch.argmax()`
- [ ] 矩阵运算：`torch.mm()`, `torch.matmul()`, `@` 运算符
- [ ] 练习：实现一个简单的向量点积和矩阵乘法
- 📖 阅读:
  - [PyTorch 官方: Math Operations](https://pytorch.org/docs/stable/torch.html#math-operations)
  - [Learn PyTorch: Linear Algebra Basics](https://www.learnpytorch.io/00_pytorch_fundamentals/#fundamental-operations)
  - [d2l.ai: 2.1.4 矩阵运算](https://d2l.ai/chapter_preliminaries/ndarray.html#linear-algebra)
- 🎬 视频:
  - [3Blue1Brown: Essence of Linear Algebra EP2 (线性组合、张成空间)](https://www.youtube.com/watch?v=k7RM-ot2NWY)
- 时间: 60 分钟

### Day 5 — Tensor Reshape 与广播
- [ ] 学习 `reshape()`, `view()`, `unsqueeze()`, `squeeze()`, `permute()`, `transpose()`
- [ ] 理解广播机制（broadcasting）
- [ ] 练习：将一个 (3, 4) 的 tensor reshape 成 (4, 3), (2, 6), (1, 3, 4)
- 📖 阅读:
  - [PyTorch 官方: Tensor View](https://pytorch.org/docs/stable/tensor_view.html)
  - [NumPy Broadcasting](https://numpy.org/doc/stable/user/basics.broadcasting.html)（PyTorch 规则相同）
  - [d2l.ai: 2.1.5 广播机制](https://d2l.ai/chapter_preliminaries/ndarray.html#broadcasting)
- 🎬 视频:
  - [3Blue1Brown: Essence of Linear Algebra EP3 (矩阵与线性变换)](https://www.youtube.com/watch?v=kYB8IZa5AuE)
- 时间: 60 分钟

### Day 6 — Tensor 与 NumPy 互转
- [ ] `torch.from_numpy()` 和 `.numpy()`
- [ ] 理解共享内存问题（修改一个会影响另一个）
- [ ] GPU tensor 转 NumPy 需要先 `.cpu()`
- [ ] 练习：用 NumPy 生成数据，转成 Tensor 做计算，再转回 NumPy
- 📖 阅读:
  - [PyTorch 官方: NumPy Bridge](https://pytorch.org/tutorials/beginner/blitz/tensor_tutorial.html#converting-numpy-to-torch-tensor)
  - [Learn PyTorch: NumPy Interop](https://www.learnpytorch.io/00_pytorch_fundamentals/)
- 🎬 视频:
  - [3Blue1Brown: Essence of Linear Algebra EP4 (矩阵乘法)](https://www.youtube.com/watch?v=XkY2DOUCWMU)
- 时间: 45 分钟 + 15 分钟回顾本周内容

### Day 7 — 周复习 + 实战小项目
- [ ] 不看文档，手写以下操作：
  - 创建一个 3x3 随机矩阵
  - 对其转置
  - 与自身做矩阵乘法
  - 求每行的均值
  - 找到最大值的索引
- [ ] 记录不懂的地方，下周重点攻克
- 📖 复习材料:
  - [PyTorch 官方 Cheat Sheet](https://pytorch.org/tutorials/beginner/ptchg_sht.html)
  - [Learn PyTorch: Exercises](https://www.learnpytorch.io/00_pytorch_fundamentals/#exercises)
- 🎬 视频:
  - [3Blue1Brown: Essence of Linear Algebra EP5 (逆矩阵)](https://www.youtube.com/watch?v=uQhTuRlWMxw)
- 时间: 60 分钟

---

## 第 2 周：Autograd 与神经网络基础

### Day 8 — 自动求导基础
- [ ] 理解 `requires_grad=True` 的含义
- [ ] 学习 `backward()` 计算梯度
- [ ] 理解计算图（computation graph）
- [ ] 练习：对 `y = x^2 + 3x + 1` 求导，验证 `dy/dx = 2x + 3`
- 📖 阅读:
  - [PyTorch 官方: Autograd Tutorial](https://pytorch.org/tutorials/beginner/basics/autogradqs_tutorial.html)
  - [PyTorch 官方: Autograd Mechanics](https://pytorch.org/docs/stable/notes/autograd.html)
  - [Learn PyTorch: Autograd](https://www.learnpytorch.io/01_pytorch_workflow_fundamentals/#6-creating-our-first-model-with-pytorch)
- 🎬 视频:
  - [Karpathy: Micrograd (从零实现自动求导)](https://www.youtube.com/watch?v=VMj-3S1tku0)
- 时间: 60 分钟

### Day 9 — Autograd 进阶
- [ ] 学习 `torch.no_grad()` 上下文管理器
- [ ] 理解 `retain_graph=True` 的用途
- [ ] 学习 `grad.zero_()` 清零梯度
- [ ] 练习：实现一个简单的梯度下降，最小化 `y = (x - 3)^2`
- 📖 阅读:
  - [PyTorch 官方: torch.no_grad](https://pytorch.org/docs/stable/generated/torch.no_grad.html)
  - [d2l.ai: 2.5 自动求导](https://d2l.ai/chapter_preliminaries/autograd.html)
- 🎬 视频:
  - [3Blue1Brown: Essence of Calculus EP1 (导数的直觉)](https://www.youtube.com/watch?v=WUvTyaaNkzM)
- 时间: 60 分钟

### Day 10 — nn.Module 基础
- [ ] 学习 `nn.Module` 的结构：`__init__()` + `forward()`
- [ ] 理解参数注册（`nn.Parameter`）
- [ ] 创建第一个神经网络：单层线性回归
- 📖 阅读:
  - [PyTorch 官方: Build Model Tutorial](https://pytorch.org/tutorials/beginner/basics/buildmodel_tutorial.html)
  - [PyTorch 官方: nn.Module 源码](https://pytorch.org/docs/stable/generated/torch.nn.Module.html)
  - [Learn PyTorch: PyTorch Workflow](https://www.learnpytorch.io/01_pytorch_workflow_fundamentals/)
- 🎬 视频:
  - [Karpathy: Building makemore (前30分钟)](https://www.youtube?v?v=PaCmpygFfXo)
- 时间: 60 分钟

### Day 11 — 常用层
- [ ] `nn.Linear` — 全连接层
- [ ] `nn.ReLU`, `nn.Sigmoid`, `nn.Tanh` — 搬活函数
- [ ] `nn.Sequential` — 快速搭建网络
- [ ] 练习：搭建一个 2 层 MLP（784 → 128 → 10）
- 📖 阅读:
  - [PyTorch 官方: nn.Linear](https://pytorch.org/docs/stable/generated/torch.nn.Linear.html)
  - [PyTorch 官方: nn.ReLU](https://pytorch.org/docs/stable/generated/torch.nn.ReLU.html)
  - [PyTorch 官方: nn.Sequential](https://pytorch.org/docs/stable/generated/torch.nn.Sequential.html)
  - [d2l.ai: 3.3 线性回归的简洁实现](https://d2l.ai/chapter_linear-networks/linear-regression-scratch.html)
- 🎬 视频:
  - [3Blue1Brown: Neural Networks EP1](https://www.youtube.com/watch?v=aircAruvnKk)
- 时间: 60 分钟

### Day 12 — 损失函数
- [ ] `nn.MSELoss` — 均方误差（回归）
- [ ] `nn.CrossEntropyLoss` — 交叉熵（分类）
- [ ] `nn.BCELoss` — 二元交叉熵
- [ ] 理解 logits vs probabilities
- [ ] 练习：对随机预测计算损失
- 📖 阅读:
  - [PyTorch 官方: Loss Functions](https://pytorch.org/docs/stable/nn.html#loss-functions)
  - [PyTorch 官方: MSELoss](https://pytorch.org/docs/stable/generated/torch.nn.MSELoss.html)
  - [PyTorch 官方: CrossEntropyLoss](https://pytorch.org/docs/stable/generated/torch.nn.CrossEntropyLoss.html)
  - [d2l.ai: 4.1 Softmax回归](https://d2l.ai/chapter_linear-networks/softmax-regression.html)
- 🎬 视频:
  - [3Blue1Brown: Neural Networks EP2 (梯度下降)](https://www.youtube.com/watch?v=IHZwWFHWa-w)
- 时间: 60 分钟

### Day 13 — 优化器
- [ ] `torch.optim.SGD` — 随机梯度下降
- [ ] `torch.optim.Adam` — Adam 优化器
- [ ] 理解 `optimizer.zero_grad()` → `loss.backward()` → `optimizer.step()` 循环
- [ ] 绩习：用 SGD 训练一个线性回归模型拟合 y = 2x + 1
- 📖 阅读:
  - [PyTorch 官方: Optimizers](https://pytorch.org/docs/stable/optim.html)
  - [PyTorch 官方: Optimizer Step](https://pytorch.org/tutorials/beginner/basics/optimization_tutorial.html)
  - [d2l.ai: 11.1 优化与深度学习](https://d2l.ai/chapter_optimization/index.html)
- 🎬 视频:
  - [3Blue1Brown: Neural Networks EP3 (反向传播)](https://www.youtube.com/watch?v=Ilg3gGewQ5U)
- 时间: 60 分钟

### Day 14 — 周复习 + 完整训练循环
- [ ] 不看文档，手写完整训练循环：
  - 准备数据（y = 3x + 2 + noise）
  - 定义模型（nn.Linear）
  - 定义损失和优化器
  - 训练 1000 步
  - 打印最终参数，验证是否接近 3 和 2
- 📖 复习材料:
  - [Learn PyTorch: 01 Workflow Overview](https://www.learnpytorch.io/01_pytorch_workflow_fundamentals/)
  - [PyTorch 官方: 60 Minute Blitz](https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html)
- 🎬 视频:
  - [Karpathy: Neural Networks Zero to Hero EP2 (Micrograd 完整)](https://www.youtube.com/watch?v=VMj-3S1tku0)
- 时间: 60 分钟

---

## 第 3 周：完整项目实战

### Day 15 — DataLoader 与 Dataset
- [ ] 学习 `torch.utils.data.Dataset` 自定义数据集
- [ ] 学习 `torch.utils.data.DataLoader` 批处理
- [ ] 理解 `batch_size`, `shuffle`, `num_workers`
- 📖 阅读:
  - [PyTorch 官方: Data Tutorial](https://pytorch.org/tutorials/beginner/basics/data_tutorial.html)
  - [PyTorch 官方: Dataset 和 DataLoader](https://pytorch.org/tutorials/beginner/data_loading_tutorial.html)
  - [Learn PyTorch: Data Loading](https://www.learnpytorch.io/01_pytorch_workflow_fundamentals/#4-preparing-and-loading-data)
- 🎬 视频:
  - [freeCodeCamp PyTorch: DataLoader (约35分钟处)](https://www.youtube.com/watch?v=G_RCsL7bxWg)
- 时间: 60 分钟

### Day 16 — MNIST 数据加载
- [ ] 使用 `torchvision.datasets.MNIST` 加载数据
- [ ] 使用 `torchvision.transforms` 做预处理（ToTensor, Normalize）
- [ ] 创建 DataLoader，查看一个 batch 的 shape
- 📖 阅读:
  - [PyTorch 官方: MNIST Tutorial](https://pytorch.org/tutorials/beginner/basics/optimization_tutorial.html)
  - [torchvision.datasets.MNIST](https://pytorch.org/vision/stable/generated/torchvision.datasets.MNIST.html)
  - [torchvision.transforms](https://pytorch.org/vision/stable/transforms.html)
- 🎬 视频:
  - [freeCodeCamp PyTorch: MNIST (约40分钟处)](https://www.youtube.com/watch?v=G_RCsL7bxWg)
- 时间: 60 分钟

### Day 17 — MNIST 分类模型
- [ ] 搭建一个简单的全连接分类网络（784 → 256 → 128 → 10）
- [ ] 添加 ReLU 激活和 Dropout
- [ ] 定义损失函数和优化器
- 📖 阅读:
  - [PyTorch 官方: Build Model](https://pytorch.org/tutorials/beginner/basics/buildmodel_tutorial.html)
  - [nn.Dropout](https://pytorch.org/docs/stable/generated/torch.nn.Dropout.html)
  - [d2l.ai: 3.6 softmax回归的简洁实现](https://d2l.ai/chapter_linear-networks/softmax-regression-concise.html)
- 🎬 视频:
  - [Karpathy: Let's build GPT (前20分钟)](https://www.youtube.com/watch?v=kCc8FmEb1nY)
- 时间: 60 分钟

### Day 18 — MNIST 训练循环
- [ ] 编写训练函数（遍历 DataLoader，计算 loss，反向传播）
- [ ] 编写验证函数（计算准确率）
- [ ] 训练 5 个 epoch，打印 train loss 和 val accuracy
- 📖 阅读:
  - [PyTorch 官方: Optimization Tutorial](https://pytorch.org/tutorials/beginner/basics/optimization_tutorial.html)
  - [Learn PyTorch: Training Loop](https://www.learnpytorch.io/01_pytorch_workflow_fundamentals/#8-training-loop)
- 🎬 视频:
  - [3Blue1Brown: Neural Networks EP4 (深度学习)](https://www.youtube.com/watch?v=IHZwWFHWa-w)
- 时间: 60 分钟

### Day 19 — 模型保存与加载
- [ ] `torch.save(model.state_dict(), 'model.pth')`
- [ ] `model.load_state_dict(torch.load('model.pth'))`
- [ ] 理解 state_dict vs 整个模型的区别
- [ ] 练习：保存训练好的 MNIST 模型，重新加载并推理
- 📖 阅读:
  - [PyTorch 官方: Save and Load Model](https://pytorch.org/tutorials/beginner/basics/saveloadrun_tutorial.html)
  - [PyTorch 官方: Serialization](https://pytorch.org/docs/stable/notes/serialization.html)
- 🎬 视频:
  - [freeCodeCamp PyTorch: Save/Load (约1小时处)](https://www.youtube.com/watch?v=G_RCsL7bxWg)
- 时间: 45 分钟 + 15 分钟回顾

### Day 20 — GPU 训练
- [ ] `device = torch.device('cuda' if torch.cuda.is_available() else 'cpu')`
- [ ] `model.to(device)`, `data.to(device)`
- [ ] 对比 CPU vs GPU 训练速度
- [ ] 练习：将 MNIST 训练迁移到 GPU
- 📖 阅读:
  - [PyTorch 官方: CUDA Semantics](https://pytorch.org/docs/stable/notes/cuda.html)
  - [PyTorch 官方: Device Management](https://pytorch.org/docs/stable/tensor_attributes.html)
  - [Learn PyTorch: Device Agnostic Code](https://www.learnpytorch.io/01_pytorch_workflow_fundamentals/#device-agnostic-code)
- 🎬 视频:
  - [freeCodeCamp PyTorch: GPU Training (约1小时20分钟处)](https://www.youtube.com/watch?v=G_RCsL7bxWg)
- 时间: 60 分钟

### Day 21 — 周复习 + 完整 MNIST 项目
- [ ] 不看文档，从零完成：
  - 数据加载（MNIST + DataLoader）
  - 模型定义（nn.Module）
  - 训练循环（loss + optimizer + epoch）
  - 验证（accuracy）
  - 保存模型
- [ ] 目标：test accuracy > 95%
- 📖 完整参考:
  - [PyTorch 官方: 60 Minute Blitz 完整版](https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html)
  - [Learn PyTorch: 02 Classification](https://www.learnpytorch.io/02_pytorch_binary_classification/)
- 🎬 视频:
  - [Karpathy: Let's build GPT (前45分钟)](https://www.youtube.com/watch?v=kCc8FmEb1nY)
- 时间: 60 分钟

---

## 第 4 周：CNN 与进阶

### Day 22 — 卷积基础
- [ ] `nn.Conv2d` — 二维卷积层
- [ ] 理解 kernel_size, stride, padding
- [ ] 可视化卷积操作（对一张图片做卷积看效果）
- 📖 阅读:
  - [PyTorch 官方: nn.Conv2d](https://pytorch.org/docs/stable/generated/torch.nn.Conv2d.html)
  - [d2l.ai: 6.2 互相关运算](https://d2l.ai/chapter_convolutional-neural-networks/conv-layer.html)
  - [Stanford CS231n: Convolutional Neural Networks](https://cs231n.github.io/convolutional-networks/)
- 🎬 视频:
  - [3Blue1Brown: But what is a Convolution?](https://www.youtube.com/watch?v=KuXjwB4LzSA)
  - [freeCodeCamp: CNN Explained](https://www.youtube.com/watch?v=pj9-LLaB_28)
- 时间: 60 分钟

### Day 23 — 池化与 BatchNorm
- [ ] `nn.MaxPool2d`, `nn.AvgPool2d`
- [ ] `nn.BatchNorm2d`
- [ ] 理解为什么需要 BatchNorm（加速训练、稳定梯度）
- 📖 阅读:
  - [PyTorch 官方: nn.MaxPool2d](https://pytorch.org/docs/stable/generated/torch.nn.MaxPool2d.html)
  - [PyTorch 官方: nn.BatchNorm2d](https://pytorch.org/docs/stable/generated/torch.nn.BatchNorm2d.html)
  - [d2l.ai: 6.5 汇聚层](https://d2l.ai/chapter_convolutional-neural-networks/pooling.html)
  - [d2l.ai: 7.5 批量归一化](https://d2l.ai/chapter_convolutional-modern/batch-norm.html)
- 🎬 视频:
  - [StatQuest: Batch Normalization](https://www.youtube.com/watch?v=DtEq44FTPM8)
- 时间: 60 分钟

### Day 24 — CNN 实现
- [ ] 搭建一个简单的 CNN：Conv → ReLU → Pool → Conv → ReLU → Pool → FC → Output
- [ ] 用 MNIST 数据训练
- [ ] 对比全连接网络 vs CNN 的参数量和准确率
- 📖 阅读:
  - [PyTorch 官方: Training a Classifier](https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html)
  - [d2l.ai: 6.6 卷积神经网络 (LeNet)](https://d2l.ai/chapter_convolutional-neural-networks/lenet.html)
  - [Stanford CS231n: Architectures](https://cs231n.github.io/convolutional-networks/)
- 🎬 视频:
  - [Karpathy: Building makemore Part 3 (RNN/CNN)](https://www.youtube.com/watch?v=PaCmpygFfXo)
- 时间: 60 分钟

### Day 25 — CIFAR-10 挑战
- [ ] 加载 CIFAR-10 数据集（10 类彩色图片）
- [ ] 调整 CNN 结构适应 32x32x3 输入
- [ ] 训练并观察准确率
- 📖 阅读:
  - [PyTorch 官方: CIFAR10 Tutorial](https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html)
  - [torchvision.datasets.CIFAR10](https://pytorch.org/vision/stable/generated/torchvision.datasets.CIFAR10.html)
  - [d2l.ai: 7.1 AlexNet](https://d2l.ai/chapter_convolutional-modern/alexnet.html)
- 🎬 视频:
  - [freeCodeCamp: CNN with PyTorch](https://www.youtube.com/watch?v=pj9-LLaB_28)
- 时间: 60 分钟

### Day 26 — 学习率调度与早停
- [ ] `torch.optim.lr_scheduler.StepLR` — 学习率衰减
- [ ] `torch.optim.lr_scheduler.CosineAnnealingLR` — 余弦退火
- [ ] 实现简单的早停机制（验证集 loss 不降就停）
- 📖 阅读:
  - [PyTorch 官方: Learning Rate Scheduler](https://pytorch.org/docs/stable/optim.html#how-to-adjust-learning-rate)
  - [d2l.ai: 11.8 学习率调度器](https://d2l.ai/chapter_optimization/lr-scheduler.html)
  - [PyTorch: CosineAnnealingLR](https://pytorch.org/docs/stable/generated/torch.optim.lr_scheduler.CosineAnnealingLR.html)
- 🎬 视频:
  - [StatQuest: Learning Rate Schedules](https://www.youtube.com/watch?v=QzulmoOgJJE)
- 时间: 60 分钟

### Day 27 — 数据增强
- [ ] `torchvision.transforms.RandomHorizontalFlip`
- [ ] `torchvision.transforms.RandomCrop`
- [ ] `torchvision.transforms.ColorJitter`
- [ ] 对比有无数据增强的 CIFAR-10 准确率
- 📖 阅读:
  - [PyTorch 官方: Transforms](https://pytorch.org/vision/stable/transforms.html)
  - [torchvision.transforms.RandomHorizontalFlip](https://pytorch.org/vision/stable/generated/torchvision.transforms.RandomHorizontalFlip.html)
  - [d2l.ai: 12.1 图像增广](https://d2l.ai/chapter_computer-vision/image-augmentation.html)
- 🎬 视频:
  - [freeCodeCamp: Data Augmentation](https://www.youtube.com/watch?v=pj9-LLaB_28)
- 时间: 60 分钟

### Day 28 — TensorBoard 可视化
- [ ] 安装 TensorBoard（`pip install tensorboard`）
- [ ] 使用 `torch.utils.tensorboard.SummaryWriter`
- [ ] 记录 loss、accuracy、learning rate
- [ ] 在浏览器中查看训练曲线
- 📖 阅读:
  - [PyTorch 官方: TensorBoard Tutorial](https://pytorch.org/tutorials/intermediate/tensorboard_tutorial.html)
  - [TensorBoard 官方文档](https://www.tensorflow.org/tensorboard/get_started)
  - [torch.utils.tensorboard](https://pytorch.org/docs/stable/tensorboard.html)
- 🎬 视频:
  - [freeCodeCamp: TensorBoard](https://www.youtube.com/watch?v=V2wJCOOCq3U)
- 时间: 60 分钟

### Day 29 — 自定义训练技巧
- [ ] 梯度裁剪（`torch.nn.utils.clip_grad_norm_`）
- [ ] 混合精度训练（`torch.cuda.amp`）
- [ ] 权重初始化（`nn.init.xavier_uniform_`）
- 📖 阅读:
  - [PyTorch 官方: Gradient Clipping](https://pytorch.org/docs/stable/generated/torch.nn.utils.clip_grad_norm_.html)
  - [PyTorch 官方: AMP Tutorial](https://pytorch.org/tutorials/recipes/recipes/amp_recipe.html)
  - [PyTorch 官方: Weight Initialization](https://pytorch.org/tutorials/beginner/examples_nn/two_layer_net_nn.html#initialize-weights)
  - [d2l.ai: 4.8 数值稳定性和模型初始化](https://d2l.ai/chapter_multilayer-perceptrons/numerical-stability.html)
- 🎬 视频:
  - [Karpathy: Let's build GPT (混合精度部分)](https://www.youtube.com/watch?v=kCc8FmEb1nY)
- 时间: 60 分钟

### Day 30 — 总复习 + 下阶段准备
- [ ] 回顾所有笔记，标记薄弱环节
- [ ] 尝试不看文档搭建一个完整 CNN 训练 CIFAR-10
- [ ] 准备进入第二阶段：从零实现 Transformer
- 📖 下阶段预习:
  - [Stanford CS336: Language Modeling from Scratch](https://cs336.stanford.edu/spring2025/)
  - [CS336 Assignment 1](https://github.com/stanford-cs336/assignment1-basics)
  - [Karpathy: Let's build GPT (完整版)](https://www.youtube.com/watch?v=kCc8FmEb1nY)
  - [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/)
- 🎬 视频:
  - [Karpathy: Let's build GPT (完整2小时)](https://www.youtube.com/watch?v=kCc8FmEb1nY)
- 时间: 60 分钟

---

## 学习原则

1. **不使用 AI 辅助写代码** — 模拟面试环境，锻炼肌肉记忆
2. **每天写代码** — 1 小时全部用于动手，不只看不写
3. **记录笔记** — 每天学完记录关键概念和踩坑点
4. **先跑通再优化** — 先让代码能跑，再考虑效率和优雅

## 核心资源汇总

| 资源 | 链接 |
|------|------|
| PyTorch 官方教程 | https://pytorch.org/tutorials/ |
| 60 Minute Blitz | https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html |
| Learn PyTorch | https://www.learnpytorch.io/ |
| Karpathy: Zero to Hero | https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ |
| 3Blue1Brown: Neural Networks | https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi |
| 3Blue1Brown: Linear Algebra | https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi |
| 3Blue1Brown: Calculus | https://www.youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr |
| d2l.ai (动手学深度学习) | https://d2l.ai/ |
| freeCodeCamp PyTorch | https://www.youtube.com/watch?v=G_RCsL7bxWg |
| Karpathy: Let's build GPT | https://www.youtube.com/watch?v=kCc8FmEb1nY |
| Karpathy: Micrograd | https://www.youtube.com/watch?v=VMj-3S1tku0 |
| Stanford CS231n | https://cs231n.github.io/ |
| The Illustrated Transformer | https://jalammar.github.io/illustrated-transformer/ |

---

创建日期: 2026-06-26
