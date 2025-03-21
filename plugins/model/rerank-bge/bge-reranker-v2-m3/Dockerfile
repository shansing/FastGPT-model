FROM pytorch/pytorch:2.1.2-cuda12.1-cudnn8-runtime

# please download the model from https://huggingface.co/BAAI/bge-reranker-v2-m3 and put it in the same directory as Dockerfile
COPY ./bge-reranker-v2-m3 ./bge-reranker-v2-m3

COPY requirements.txt .

RUN python3 -m pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

COPY app.py Dockerfile .

ENTRYPOINT python3 app.py
