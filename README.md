# 🥷 Block Ninja Game
Ein kleines aber feines Web-Game (https://codepen.io/Feeling_Stobby/pen/WNNaKVp) – deployed via CI/CD auf AWS ECS Fargate 🚀


Steuerung:

Bewegen mit der Maus
Schneiden mit links-click


Diese Pipeline ist:

automatisch (CI/CD)
stabil & portabel (Docker)
sicher & Cloud-ready (ECR/ECS)
einfach wartbar (GitHub Actions + Fargate)
skalierbar (AWS Architektur)

---

## 📦 Features

- HTML/CSS/JS Game
- Containerisiert mit Docker
- Automatische CI/CD-Pipeline mit GitHub Actions
- Deployment auf AWS ECS (Fargate) via ECR
- Kein Load Balancer – direkter Zugriff via Public IP

---

## 🛠️ Setup

1. Klone das Repo:
```bash
git clone https://github.com/armin-backhaus/block-ninja-game.git


Lokales Testen mit Docker:

docker build -t block-ninja-game .
docker run -p 8080:80 block-ninja-game

👉 Öffne im Browser: http://localhost:8080


⚙️ CI/CD Workflow
Die Datei .github/workflows/deploy.yml steuert den automatischen Build- und Deployment-Prozess:

✅ Code Push auf main
🐳 Docker Image Build
☁️ Push nach Amazon ECR
🔁 Update der ECS Task Definition
🚀 Re-Deployment auf ECS Fargate




🧱 Infrastruktur (AWS)
Komponente	Name
ECS Cluster	block-ninja-cluster
ECS Service	block-ninja-service
ECR Repo	block-ninja-game
IAM Role	ecsTaskExecutionRole
Deployment Methode	GitHub Actions


🔗 Zugriff
👉 Aktueller Zugriff über die Public IP der ECS Task (kein ALB).




👨‍💻 Game-Autor
    Block Ninja!
👾 Jeve Stobs

👨‍💻 CI/CD-Autor
👾 armin-backhaus
