FROM ubuntu

WORKDIR /app

COPY . .

SHELL ["/bin/bash", "-c"]

RUN apt-get update && \
    apt-get install -y python3 python3-pip python3-venv && \
    python3 -m venv venv1 && \
    source venv1/bin/activate && \
    pip install --no-cache-dir -r requirements.txt

EXPOSE 5000

CMD [ "/bin/bash", "-c", "source venv1/bin/activate && python3 app.py" ]
