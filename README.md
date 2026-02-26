# 🎵 music_recommender

A cloud-based music recommendation system built entirely in **Python**, split across three independent microservices. Each service handles a specific part of the pipeline, making the whole thing modular and easy to scale or swap out.

Sample MP3 files are included in the repo so you can test the system without needing your own audio files right away.



## how it works

The project follows a microservices architecture — each service does one thing and hands off to the next:

- **service_1** — handles the input side, likely audio ingestion or user request handling
- **service_2** — the core logic, probably feature extraction or the recommendation engine itself
- **service_3** — deals with output, such as returning results or serving recommendations

> since the services are decoupled, you can run them independently or wire them together depending on your setup.



## getting started

### 1. clone the repo

```bash
git clone https://github.com/abtin4079/music_recommender.git
cd music_recommender
```

### 2. set up a virtual environment (recommended)

```bash
python -m venv venv
source venv/bin/activate  # on Windows: venv\Scripts\activate
```

### 3. install dependencies

Each service may have its own requirements. Check inside each folder:

```bash
cd service_1 && pip install -r requirements.txt
cd ../service_2 && pip install -r requirements.txt
cd ../service_3 && pip install -r requirements.txt
```

### 4. run a service

```bash
cd service_1
python main.py
```

Repeat for the other services as needed. The included `.mp3` files can be used as test inputs.



## project structure

```
service_1/        # service one (input / ingestion)
service_2/        # service two (recommendation logic)
service_3/        # service three (output / results)
TRACK01.MP3       # sample audio file for testing
13_-_him_i_-_...  # another sample track
```



## built with

- **Python** — 100% of the codebase
- **Microservices architecture** — loosely coupled, independently runnable services
- Designed as a cloud project (`Cloud_project1`)



👤 made by [abtin4079](https://github.com/abtin4079)
