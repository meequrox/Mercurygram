FROM python:latest

WORKDIR /p2p-gateway

RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y python3-starlette python3-httpx python3-uvloop python3-aiofiles uvicorn

COPY main.py ./

EXPOSE 80

ENTRYPOINT ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]
