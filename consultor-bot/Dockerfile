FROM python:3.12-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt && rm -rf /root/.cache/pip
COPY . .
ENTRYPOINT ["python", "src/main.py"]
CMD ["--help"]
