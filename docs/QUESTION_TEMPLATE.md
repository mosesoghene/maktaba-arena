# 📝 Question Contribution Template

To ensure the game can easily read and display questions during a live match, we use a simple text format called JSON. 

You do not need to be a programmer to add questions! Just copy the template below, fill in your knowledge, and submit it to the `/data/subjects/` folder.

## 🏗️ The Structure

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
  "explanation": "A brief explanation of why the answer is correct (Optional)"
}