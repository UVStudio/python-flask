### deployment

API is deployed on Render.com

### runs app in docker locally and refreshes on save

```
docker run -dp 5005:5000 -w /app -v "$(pwd):/app" flask-smorest-api
```

### activate venv

```
source .venv/bin/activate
```

### create flask-smorest-api Docker Image

```
docker build -t flask-smorest-api .
```

### Dockerfile for local dev

```
FROM python:3.11
EXPOSE 5000
WORKDIR /app
COPY ./requirements.txt requirements.txt
RUN pip install --no-cache-dir --upgrade -r requirements.txt
COPY . .
CMD ["flask", "run", "--host", "0.0.0.0"]
```

### .env

```
DATABASE_URL=
JWT_SECRET_KEY=
```
