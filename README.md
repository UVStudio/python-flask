### runs app in docker and refreshes on save

docker run -dp 5005:5000 -w /app -v "$(pwd):/app" flask-smorest-api

### activate venv

source .venv/bin/activate

### create flask-smorest-api Docker Image

docker build -t flask-smorest-api .
