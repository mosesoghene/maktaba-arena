# 🗄️ Maktaba Arena: Data & Question Banks

This directory contains the raw JSON data that powers the game's knowledge base. 

The `subjects/` folder holds categorized question lists. When setting up the environment, the Django backend will use a custom management command to read these JSON files and bulk-insert the questions into the PostgreSQL database.

**Want to add questions?** Please refer to the `QUESTION_TEMPLATE.md` located in the `/docs` folder for the exact JSON format required.
