# HearSay Mind 

Backend de la solution HearSay, une application de visioconférence assistée par IA avec reconnaissance de gestes et langage des signes.

---

## Technologies

- Python 3.10+
- FastAPI
- MediaPipe (gestes main)
- PyTorch / TensorFlow (modèle ASL)
- TTS (Coqui TTS ou Google TTS)
- WebSocket pour communication temps réel
- Docker & Docker Compose

---

## Structure du projet

```

hearsay-backend/
├── app/
│   ├── main.py
│   ├── routes/
│   │   ├── gesture\_control.py
│   │   ├── sign\_detect.py
│   │   ├── tts.py
│   │   └── ws\_handler.py
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
└── .gitignore

````

---

## Installation

1. Cloner le repo

```bash
git clone https://github.com/Rochdi112/hearsay-backend.git
cd hearsay-backend
````

2. Construire et lancer avec Docker

```bash
docker-compose up --build
```

3. Ou installer les dépendances localement

```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
.\venv\Scripts\activate   # Windows
pip install -r requirements.txt
uvicorn app.main:app --reload
```

---

## Endpoints principaux

* `GET /` : Accueil, test API
* `POST /gesture-control/` : Endpoint gestuel
* `POST /sign-detect/` : Détection alphabet langue des signes
* `POST /speak/` : Synthèse vocale
* WebSocket `/ws/gesture` : commandes gestuelles en temps réel

---


## Licence

MIT © HearSay Team

---
