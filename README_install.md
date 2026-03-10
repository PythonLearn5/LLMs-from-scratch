# 安装环境

### 安装 pymanager-260

https://www.python.org/downloads/release/pymanager-260/

下载安装 最新版python


pip install uv

uv venv --python=python3.10

Set-ExecutionPolicy RemoteSigned -Scope CurrentUser

### 激活虚拟环境
linux:  source .venv/bin/activate
windows:.venv\Scripts\Activate.ps1

python --version

### 安装 软件包

激活虚拟环境后，您可以使用以下命令安装 Python 包uv。
uv pip install packaging
安装所有必需的软件包
uv pip install -r requirements.txt


注意： 如果由于某些依赖项（例如，如果您使用的是 Windows 系统）而导致上述命令出现问题，您可以始终回退到使用常规的 
pip： pip install -r requirements.txt 或 
pip install -U -r https://raw.githubusercontent.com/rasbt/LLMs-from-scratch/refs/heads/main/requirements.txt

附加材料的可选依赖项
uv pip install --group bonus

### 运行测试脚本

python setup/02_installing-python-libraries/python_environment_check.py

运行 Notebook

在项目目录执行：
jupyter lab
浏览器会打开 **JupyterLab。

然后进入：

LLMs-from-scratch
└─ ch02
└─ *.ipynb

点击 Notebook 后：
Shift + Enter
逐块运行代码。

依赖库说明

| 分类           | 库          | 主要作用            | 说明                           |
| ------------ | ---------- | --------------- | ---------------------------- |
| 深度学习框架       | PyTorch    | 构建和训练神经网络       | 本书 GPT / Transformer 主要实现框架  |
|              | TensorFlow | 深度学习框架          | 用于部分示例或对比                    |
| 数学计算         | NumPy      | 高性能数组和矩阵计算      | 深度学习底层数学计算基础                 |
| 数据处理         | Pandas     | 表格数据处理          | 数据清洗、CSV读取、统计分析              |
| Tokenization | tiktoken   | 文本转 token ID    | OpenAI tokenizer，用于 LLM 输入编码 |
| Notebook 环境  | JupyterLab | 交互式 Notebook 环境 | 运行 `.ipynb`，AI研究常用           |
| 可视化          | Matplotlib | 数据可视化绘图         | 画 loss 曲线、attention 图        |
| 训练辅助         | tqdm       | 进度条工具           | 显示训练或处理进度                    |
| 系统监控         | psutil     | 系统资源监控          | 获取 CPU / 内存使用情况              |

在 LLMs-from-scratch 中的作用结构
LLM项目运行环境
│
├─ 深度学习
│   ├─ PyTorch
│   └─ TensorFlow
│
├─ 数学计算
│   └─ NumPy
│
├─ 数据处理
│   └─ Pandas
│
├─ 文本处理
│   └─ tiktoken
│
├─ 可视化
│   └─ Matplotlib
│
├─ 训练辅助
│   └─ tqdm
│
├─ 系统监控
│   └─ psutil
│
└─ Notebook运行环境
└─ JupyterLab

### AI / LLM 项目常见 Python 技术栈全景表

| 分类            | 常见库                       | 主要作用          | 说明               |
| ------------- | ------------------------- | ------------- | ---------------- |
| 深度学习框架        | PyTorch                   | 构建和训练神经网络     | 当前 AI / LLM 主流框架 |
|               | TensorFlow                | 深度学习框架        | Google 出品        |
|               | JAX                       | 高性能数值计算       | Google 新一代 ML 框架 |
| 数学计算          | NumPy                     | 矩阵 / 数组计算     | Python 科学计算基础    |
|               | SciPy                     | 科学计算算法        | 线性代数 / 优化        |
| 数据处理          | Pandas                    | 表格数据处理        | CSV / Excel      |
|               | Polars                    | 高性能数据处理       | Pandas 替代        |
| Tokenization  | tiktoken                  | 文本 token 编码   | OpenAI tokenizer |
|               | SentencePiece             | 子词分词算法        | Google tokenizer |
| Transformer生态 | Hugging Face Transformers | 预训练模型库        | GPT / BERT       |
|               | Accelerate                | 分布式训练         | 多 GPU            |
|               | PEFT                      | 参数高效微调        | LoRA 等           |
| 数据集           | Hugging Face Datasets     | AI 数据集管理      | NLP 数据           |
|               | TensorFlow Datasets       | 数据集工具         | Google           |
| 可视化           | Matplotlib                | 绘图            | 基础图形             |
|               | Seaborn                   | 高级统计图         | 数据分析             |
|               | Plotly                    | 交互式图表         | Web 可视化          |
| Notebook环境    | JupyterLab                | Notebook IDE  | AI研究常用           |
|               | Google Colab              | 云 Notebook    | 免费 GPU           |
| 训练辅助          | tqdm                      | 进度条           | 训练进度             |
|               | psutil                    | 系统资源监控        | CPU / 内存         |
|               | Weights & Biases          | 训练日志平台        | ML 实验管理          |
| GPU加速         | CUDA                      | NVIDIA GPU 计算 | 深度学习加速           |
|               | cuDNN                     | GPU神经网络库      | NVIDIA           |
| LLM推理         | vLLM                      | 高性能 LLM 推理    | 高并发              |
|               | llama.cpp                 | 本地 LLM 推理     | CPU / GPU        |
| 向量数据库         | FAISS                     | 向量搜索          | Meta             |
|               | Milvus                    | 向量数据库         | AI检索             |
| AI应用框架        | LangChain                 | LLM应用开发       | RAG / Agent      |
|               | LlamaIndex                | 知识库检索         | RAG              |
| Web部署         | FastAPI                   | AI接口服务        | Python API       |
|               | Gradio                    | AI Demo UI    | 模型展示             |
|               | Streamlit                 | AI Web App    | 快速展示             |
