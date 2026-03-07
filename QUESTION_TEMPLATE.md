# 📝 Question Contribution Template

Welcome to the question bank for **Maktaba Arena**! 

To ensure the game can easily read, shuffle, and display the questions during a live match, we use a simple text format called JSON (JavaScript Object Notation). 

You do not need to be a programmer to add questions! Just copy the template below, fill in your knowledge, and submit it.

---

## 🏗️ The Structure

Each subject (e.g., `math.json`, `chemistry.json`, `social_studies.json`) lives in the `/data/subjects/` folder and contains a list of questions. 

Here is the exact structure you need to use for a single question:

```json
{
  "topic": "The specific area of the subject",
  "difficulty": "easy, medium, or hard",
  "question": "The question you want to ask the players",
  "options": [
    "Option A",
    "Option B",
    "Option C",
    "Option D"
  ],
  "correct_answer": "Must exactly match the text of one of the options above",
  "explanation": "A brief explanation of why the answer is correct (Optional, but highly encouraged for learning!)"
}

```

---

## 💡 Examples

Here are a few examples of what finished questions look like.

### Example 1: Math

```json
{
  "topic": "Algebra",
  "difficulty": "easy",
  "question": "What is the value of x if 2x + 6 = 14?",
  "options": [
    "2",
    "4",
    "6",
    "8"
  ],
  "correct_answer": "4",
  "explanation": "Subtract 6 from 14 to get 8. Divide 8 by 2 to get x = 4."
}

```

### Example 2: Social Studies

```json
{
  "topic": "African Geography",
  "difficulty": "medium",
  "question": "Which of these rivers is the longest in Africa?",
  "options": [
    "River Niger",
    "Congo River",
    "Nile River",
    "Zambezi River"
  ],
  "correct_answer": "Nile River",
  "explanation": "The Nile River is the longest river in Africa, stretching over 6,600 kilometers."
}

```

---

## 📬 How to Submit Your Questions

1. **Find the Right File:** Go to the `/data/subjects/` folder and open the JSON file for your subject. If one doesn't exist yet, feel free to create it (e.g., `music.json`).
2. **Add Your Data:** Paste your new question(s) inside the square brackets `[ ]`.
3. **Check Your Commas:** Make sure every question block is separated by a comma `,` (except the very last one).
4. **Submit:** Save your changes and open a Pull Request.

**Not comfortable with GitHub or JSON?** No problem! You can go to the **Issues** tab, click "New Issue," use the `new-questions` tag, and simply type out your questions in plain text. One of our developers will format it and add it to the game for you.

