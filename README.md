# 📚 Maktaba Arena

Maktaba Arena (Swahili for "Library Arena") is an open-source, real-time multiplayer educational game designed to make learning competitive, collaborative, and fun. 

Built to solve educational engagement challenges, Maktaba Arena allows players and teams to test their knowledge across multiple subjects like Math, Chemistry, Social Studies, Arts, and Music. Whether played on a single interactive smart screen in a classroom or across multiple devices globally, it turns education into an engaging e-sport.

---

## 🚀 Core Features

* **Real-Time Multiplayer:** Compete globally or locally in single-player or N-player teams using WebSocket-driven gameplay.
* **Single-Screen Mode:** Optimized UI for classroom play, smart boards, and projector setups (e.g., Wowbi screens) to view live scores and team standings.
* **Custom Competitions:** Game Admins (schools, teachers, or event organizers) can create custom accounts, define new subjects, and build private question banks.
* **Global Matchmaking:** Match with players worldwide based on specific subject interests and skill levels.
* **Player Dashboards:** Track personal and team statistics, including global wins, lowest fails, and subject mastery over time.

---

## 🛠️ Tech Stack & Architecture

Maktaba Arena is built with a modern, scalable architecture designed for easy deployment and robust server management:

* **Frontend:** React (for a dynamic, responsive user interface)
* **Backend:** Python / Django (handling business logic, APIs, and real-time WebSockets via Django Channels)
* **Database:** PostgreSQL (relational data storage for users, questions, and match history)
* **Infrastructure:** Docker & Docker Compose (containerized for seamless local development and production deployment)

---

## 🏁 Getting Started

To get a local copy up and running, follow these simple steps. Because the entire environment is containerized, you won't need to install Python or Node.js locally—just Docker.

### Prerequisites

* [Docker](https://docs.docker.com/get-docker/)
* [Docker Compose](https://docs.docker.com/compose/install/)
* Git

### Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/maktaba-arena.git](https://github.com/yourusername/maktaba-arena.git)
   cd maktaba-arena

   ```

2. **Build and spin up the containers:**
```bash
docker-compose up --build -d

```


3. **Run database migrations:**
```bash
docker-compose exec backend python manage.py migrate

```


4. **Create a superuser for the admin dashboard:**
```bash
docker-compose exec backend python manage.py createsuperuser

```



Once running, access the React frontend at `http://localhost:3000` and the Django backend API / Admin panel at `http://localhost:8000`.

---

## 🗺️ Project Roadmap

Maktaba Arena is actively in development. Our current sprint roadmap includes:

* [ ] **Phase 1:** Foundation & Architecture (Repo setup, Docker config, UI wireframes)
* [ ] **Phase 2:** Core API & Admin Features (Auth, CRUD APIs for Subjects/Questions)
* [ ] **Phase 3:** Real-Time Engine (WebSocket integration, Matchmaking logic, Game Loop)
* [ ] **Phase 4:** Player Experience (Dashboards, Leaderboards, Single-Screen UI)
* [ ] **Phase 5:** Open-Source Polish (Load testing, CI/CD pipelines, Beta launch)

---

## 🤝 Contributing to Maktaba Arena

We welcome contributions from developers, educators, and designers! It takes a village to build a massive educational platform. Here is how you can help:

### For Educators & Subject Experts (No Coding Required!)

We are always expanding our question banks. You don't need to be a programmer to contribute knowledge.

1. Navigate to the `/data/subjects` folder in this repository.
2. Follow the JSON format outlined in the `QUESTION_TEMPLATE.md` to add new questions for any subject.
3. Submit a Pull Request (PR) with your additions.

### For Developers

1. Check our **Issue Tracker** for tasks tagged `good first issue` or `help wanted`.
2. Fork the repository and create your feature branch: `git checkout -b feature/AmazingFeature`.
3. Commit your changes: `git commit -m 'Add some AmazingFeature'`.
4. Ensure your code passes all linting and containerized tests.
5. Push to the branch: `git push origin feature/AmazingFeature`.
6. Open a Pull Request.

### Reporting Bugs

If you find a bug, please open an issue and include:

* Your operating system and browser.
* Steps to reproduce the bug.
* What you expected to happen vs. what actually happened.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

## 📫 Contact

**Project Maintainer:** [Your Name/Handle] - [@YourTwitter](https://www.google.com/search?q=https://twitter.com/yourtwitter) - email@example.com

**Project Link:** [https://github.com/mosesoghene/maktaba-arena](https://github.com/mosesoghene/maktaba-arena)

