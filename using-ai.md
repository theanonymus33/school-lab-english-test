# Using AI with this project

## What the app does and does not use AI for

The app itself does **not** call any AI service. Speaking marks come from a free keyword and length check in the page, so it costs nothing and works without accounts. That check is only a first pass and the teacher can override every mark.

## Using an AI assistant to write your questions (free options work)

Any chat assistant (Claude, ChatGPT, Gemini and others) can draft questions for you. You then paste them into the CSV and upload it.

1. Open the downloaded `A2_Question_Bank.csv` to see the format.
2. Give the assistant a prompt like the one below, fill in the brackets.
3. Ask for **CSV output only**, paste it into a new file, and save as `.csv`.
4. Upload it in **Question Bank**. The app reports any row that is wrong.
5. **Read every question yourself.** AI can make mistakes, such as a wrong answer key or two correct options.

### Prompt you can copy

```
Create a question bank as CSV for English learners at CEFR A2 level, [class/age group].
Use exactly these columns in the first row:
section,question,option_a,option_b,option_c,option_d,correct,audio_text,passage,keywords

Make:
- [10] listening rows: short spoken announcements (1-2 sentences) in audio_text. The question must be answerable only by hearing the text. 4 options, one correct, correct = A, B, C or D.
- [10] reading rows: a 2-3 sentence passage in the passage column, one question about it, 4 options, correct = A, B, C or D.
- [10] speaking rows: short direct questions about [topics: school, family, hobbies, food, festivals]. Put 8-15 words a good answer would contain in keywords, separated by semicolons.
- [3] writing rows: simple writing tasks of 4-5 lines.

Rules: simple A2 vocabulary, no trick questions, only one correct option, answers placed in a mix of positions A-D, leave unused columns empty, put text containing commas inside double quotes. Output only the CSV, no explanation.
```

### Check list before uploading
- Exactly one option is correct for every listening and reading question.
- The listening `audio_text` really contains the answer, and the reading `passage` does too.
- The correct letters are not all the same.
- Nothing culturally or age inappropriate.

## Ways to use AI to improve the project itself

- Ask an AI coding assistant to add a feature (for example more question types) by giving it `index.html` and a clear description. Test the result on one computer before using it in class.
- Ask it to review the file for bugs, accessibility problems or spelling mistakes.
- Ask it to translate the interface text into your local language.

## If you later want AI marking for speaking

This would need an internet connection and a paid API key from an AI provider, and the key would have to be kept away from students (a key stored in a web page can be read by anyone with developer tools). A safer design uses a small server owned by the school. This project does not include that, to keep it free and simple.

## Student privacy with AI tools

Do not paste real student names, marks or recordings into public AI tools. Use made-up examples when you ask for help.
