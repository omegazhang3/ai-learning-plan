# Day 1 — 环境搭建 + PyTorch 安装

**日期**: 2026-06-26  
**设备**: MacBook Pro Apple M4 Pro  
**Python**: 3.9.6 (macOS 自带)  
**用时**: ~30 分钟

---

## 执行过程

### 1. 检查 Python 环境

```bash
python3 --version
# Python 3.9.6
```

macOS 自带 Python 3.9.6，使用 `pip3` 代替 `pip`。

### 2. 安装 PyTorch

```bash
pip3 install torch torchvision torchaudio
```

安装成功，输出警告：

```
WARNING: The scripts torchfrtrace and torchrun are installed in
'/Users/I309571/Library/Python/3.9/bin' which is not on PATH.
```

### 3. 修复 PATH 警告

```bash
echo 'export PATH="$HOME/Library/Python/3.9/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

### 4. 验证 PyTorch 安装

```bash
python3 -c "import torch; print('PyTorch:', torch.__version__); print('MPS:', torch.backends.mps.is_available())"
```

输出：

```
PyTorch: <module 'torch.version' from '/Users/I309571/Library/Python/3.9/lib/python/site-packages/torch/version.py'>
MPS: True
```

✅ PyTorch 已安装，MPS（Apple Silicon GPU）已启用。

### 5. 验证 MPS GPU 计算

```bash
python3 -c "import torch; x=torch.randn(3,3,device='mps'); y=torch.randn(3,3,device='mps'); z=x@y; print('MPS 计算结果:'); print(z); print('设备:', z.device)"
```

输出：

```
MPS 计算结果:
tensor([[ 1.3035,  2.3175, -0.4412],
        [ 0.1337,  1.4971,  0.3683],
        [-0.4093, -3.9234,  0.4053]], device='mps:0')
设备: mps:0
```

✅ M4 Pro GPU 计算正常工作，设备显示为 `mps:0`。

---

## 关键知识点

### Apple Silicon + PyTorch

| 项目 | 说明 |
|------|------|
| **MPS 后端** | PyTorch 原生支持 Apple Silicon GPU（Metal Performance Shaders） |
| **设备标识** | `torch.device("mps")` 或 `device='mps:0'` |
| **M4 Pro** | 12核 CPU + 20核 GPU + 16核 Neural Engine |
| **统一内存** | CPU/GPU 共享内存，无需数据拷贝 |

### 代码差异（MPS vs CUDA）

```python
# NVIDIA GPU (服务器)
device = torch.device('cuda' if torch.cuda.is_available() else 'cpu')

# Apple Silicon (MacBook Pro)
device = torch.device('mps' if torch.backends.mps.is_available() else 'cpu')
```

### pip vs pip3

macOS 自带的 Python 环境中，`pip` 通常不可用，需要用 `pip3` 或 `python3 -m pip`。

---

## 遇到的问题与解决

| 问题 | 原因 | 解决方案 |
|------|------|----------|
| `zsh: command not found: pip` | macOS 自带 Python 不配置 `pip` | 使用 `pip3` 代替 |
| torchrun 不在 PATH | 安装脚本目录未加入 PATH | `echo 'export PATH="$HOME/Library/Python/3.9/bin:$PATH"' >> ~/.zshrc` |
| 多行 Python 代码 IndentationError | zsh 多行字符串缩进问题 | 改用单行 `python3 -c "..."` 写法 |

---

## 环境信息记录

```
设备: MacBook Pro Apple M4 Pro
Python: 3.9.6
PyTorch: 已安装
MPS: 可用 (mps:0)
pip 路径: ~/Library/Python/3.9/bin
site-packages: ~/Library/Python/3.9/lib/python/site-packages/
```

---

## 下一步 (Day 2)

- 学习 Tensor 创建方式：`torch.tensor()`, `torch.zeros()`, `torch.ones()`, `torch.randn()`, `torch.arange()`
- 理解 shape、dtype、device 三个核心属性
- 阅读: [PyTorch 官方 Tensor Quickstart](https://pytorch.org/tutorials/beginner/basics/tensorqs_tutorial.html)

---

完成日期: 2026-06-26
