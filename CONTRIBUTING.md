# Contributing to Maktaba Arena

First off, thank you for considering contributing to Maktaba Arena! It is people like you who make this platform a powerful, globally accessible tool for students. 

Whether you are a software engineer building out the real-time WebSocket engine, a frontend developer crafting the single-screen UI, or an educator adding new chemistry questions, your contributions are incredibly valuable.

---

## 🧭 Code of Conduct

By participating in this project, you agree to abide by our Code of Conduct. We expect all contributors to maintain a welcoming, inclusive, and respectful environment for everyone.

---

## 👩‍🏫 For Educators & Subject Matter Experts

You do not need to know how to code to make a massive impact. Maktaba Arena relies on rich, accurate, and diverse question banks for subjects ranging from Math and Science to Arts and Social Studies.

### How to Add Questions
1. Navigate to the `/data/subjects/` directory in this repository.
2. Find the JSON file for the subject you want to contribute to (e.g., `chemistry.json`). If the subject doesn't exist, you can create a new file!
3. Follow the format outlined in our `QUESTION_TEMPLATE.md` to format your questions, answers, and the correct option.
4. Submit a Pull Request (PR) with your additions. 

*If you are unfamiliar with GitHub, you can also open an **Issue** with the tag `new-questions` and paste your text there. A developer will format it for you!*

---

## 💻 For Developers

Maktaba Arena utilizes a modern stack: **React (Frontend)**, **Django (Backend)**, **PostgreSQL (Database)**, and **Docker (Infrastructure)**. 

### Local Development Setup

Because the entire environment is containerized, getting started is straightforward. You only need Docker and Git installed on your system.

1. **Fork and Clone the Repository**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/maktaba-arena.git](https://github.com/YOUR_USERNAME/maktaba-arena.git)
   cd maktaba-arena

   ```

2. **Spin Up the Containers**
```bash
docker-compose up --build

```


3. **Database Setup**
Open a new terminal window and run the Django migrations inside the backend container:
```bash
docker-compose exec backend python manage.py migrate

```



### Branch Naming Conventions

Please use descriptive branch names to keep the repository organized:

* `feat/your-feature-name` (for new features)
* `bugfix/issue-description` (for bug fixes)
* `docs/update-readme` (for documentation changes)
* `content/add-math-questions` (for adding educational data)

### Making Changes

1. Check the **Issues** tab for tasks labeled `good first issue` or `help wanted`.
2. Assign the issue to yourself or leave a comment so others know you are working on it.
3. Create your branch from `main`.
4. Write clean, documented code. If you are changing Django models, ensure you generate and commit the migration files.
5. Test your changes locally to ensure both the React frontend and Django backend run seamlessly.

---

## 🐛 Reporting Bugs

If you encounter an issue while playing or hosting a game, please open an Issue using the following format:

* **Describe the Bug:** A clear and concise description of what the bug is.
* **Steps to Reproduce:** Exactly what you clicked or typed to make the bug happen.
* **Expected Behavior:** What you expected to happen instead.
* **Environment:** Your Operating System (e.g., Ubuntu, Windows 11), Browser, and whether you were running the game locally via Docker or on a live server.

---

## 🚀 Pull Request Process

1. Ensure your code aligns with the existing style and architecture.
2. Update the `README.md` if you are introducing new environment variables, Docker configurations, or major features.
3. Open a Pull Request against the `main` branch.
4. Provide a clear description of the problem you solved or the feature you added.
5. Wait for a project maintainer to review your code. We may request some changes before merging.

Thank you for helping us build the ultimate educational arena!
