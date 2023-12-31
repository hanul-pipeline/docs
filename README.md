* README.md is written in KOREAN

# 한울 프로젝트
산업 현장의 위험 요소를 관리 및 모니터링하는 데이터 기반의 솔루션 프로젝트입니다.<br><br>

# Pipeline Structure
<img width="792" alt="스크린샷 2023-12-31 오후 9 16 52" src="https://github.com/hanul-pipeline/docs/assets/130134750/1e6bd241-c0d8-4320-a1f8-e33cee4c56c8"><br><br>

# Used Stacks
### Scheduling
- Airflow (Docker 기반의 서비스 빌드) : API 서버 작업 스케줄링

### API & ETL
- FastAPI + uvicorn[standard] : ETL 프로세스 수행 & 경보 로직 수행 (LINE NOTI 경보 메세지 전송)

### Processing
- Python & Pandas : MySQL 데이터 호출 및 .parquet 파일 생성

### DL(Storage)
- MySQL : information(회사 내부 정보 데이터베이스), measurement(센서 측정값 데이터 & 경보 데이터)
- Hadoop HDFS : .parquet 데이터 및 Hive 메타데이터 저장소

### Monitoring
- Grafana: MySQL 서버 measurement 모니터링
