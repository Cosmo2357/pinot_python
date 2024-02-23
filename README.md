# Apache Pinot with Python

dev environment
Python3.11

### 仮想環境構築
```bash
python3 -m venv .venv

# Linux または macOS の場合
source .venv/bin/activate 

# Windows の場合
.venv\Scripts\activate   
```
### パッケージの一括インストール
requirements.txt に記載されたパッケージを一括でインストールします。
```bash
pip install -r requirements.txt
```

### uvicorn インストール
```bash
pip install "uvicorn[standard]"
```

### start uvicorn server
```bash

uvicorn main:app --reload
```
### API Base URL
http://127.0.0.1:8000

### Swagger UI
http://127.0.0.1:8000/docs

### ReDoc
http://127.0.0.1:8000/redoc

## Apache Pinot
### Apache Pinot docker
```bash 
# Download the latest release of Apache Pinot Docker image
docker pull apachepinot/pinot:1.0.0
```
### Apache Pinot 起動
```bash
# Start Apache Pinot with QuickStart mode
docker run \
    -p 2123:2123 \
    -p 9000:9000 \
    -p 8000:8000 \
    -p 7050:7050 \
    -p 6000:6000 \
    apachepinot/pinot:1.0.0 QuickStart \
    -type batch
  ```

### Pinot Swagger UI
http://localhost:9000/help

### Pinot UI
http://localhost:9000


# Stargate > Cassandra > Debezium > Kafka > Pinot

# Stargate > Cassandra  > Debezium > Kafka >  Elasticsearch

https://stargate.io/
https://debezium.io/