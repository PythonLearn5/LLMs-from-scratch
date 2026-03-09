# 安装环境

### 安装 pymanager-260

https://www.python.org/downloads/release/pymanager-260/

下载安装 最新版python


pip install uv

uv venv --python=python3.10

Set-ExecutionPolicy RemoteSigned -Scope CurrentUser

.venv\Scripts\Activate.ps1


### 安装 软件包

uv pip install packaging

uv pip install -r requirements.txt


注意： 如果由于某些依赖项（例如，如果您使用的是 Windows 系统）而导致上述命令出现问题，您可以始终回退到使用常规的 pip： pip install -r requirements.txt 或 pip install -U -r https://raw.githubusercontent.com/rasbt/LLMs-from-scratch/refs/heads/main/requirements.txt