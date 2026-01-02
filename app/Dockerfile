FROM python:3.12-slim

RUN useradd -m -u 10001 appuser

WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY app.py .
RUN chown -R 10001:10001 /app

USER 10001

EXPOSE 8080
CMD ["python", "app.py"]
