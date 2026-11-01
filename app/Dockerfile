FROM python:3.12-slim
WORKDIR /app
# Utilisateur non-root
RUN groupadd --system app && useradd --system --gid app --no-create-home app

COPY . .
RUN pip install --require-hashes --no-cache-dir -r requirements.txt

USER app

EXPOSE 5000
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "5000"]