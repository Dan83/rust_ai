FROM pytorch/pytorch:latest

RUN pip install torchvision

ENV PYTHONPATH=/app:$PYTHONPATH

WORKDIR /app

COPY . /app

ENTRYPOINT [ "python", "model.py" ]
