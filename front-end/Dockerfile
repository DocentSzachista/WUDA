# ADD YOUR OWN DOCKERFILE
#https://docs.docker.com/guides/python/containerize/
ARG PYTHON_VERSION=3.12
ARG SERVER_PORT=8000
FROM python:${PYTHON_VERSION}-slim
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1
WORKDIR /app
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt
COPY . /app/
EXPOSE ${SERVER_PORT}
CMD ["python", "app.py"]