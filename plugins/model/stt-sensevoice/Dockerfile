#FROM yiminger/sensevoice:latest
FROM pytorch/pytorch:2.1.2-cuda12.1-cudnn8-runtime

COPY ./app /app
# please download the model from https://huggingface.co/FunAudioLLM/SenseVoiceSmall and put it in the same directory as Dockerfile
COPY ./SenseVoiceSmall /app/iic/SenseVoiceSmall

WORKDIR /app

#COPY main.py /app/main.py

RUN pip3 install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

CMD ["python3","main.py"]
