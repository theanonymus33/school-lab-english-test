# Question file format

The question bank is a CSV file. One row is one question. Download the current file from **Teacher portal, Question Bank, Download question file**, edit it, then upload it.

Columns (keep the first row exactly as it is):

`section, question, option_a, option_b, option_c, option_d, correct, audio_text, passage, keywords`

| section | what to fill in |
|---|---|
| `listening` | `question`, at least two options, `correct` (A, B, C or D), and `audio_text` (the sentence read aloud) |
| `reading` | `question`, at least two options, `correct` (A, B, C or D), and `passage` (the text to read) |
| `speaking` | `question`, and `keywords` (words a good answer would contain, separated by `;`) |
| `writing` | `question` only |

Rules
- Each section needs at least one question. Limits: 40 listening, 20 speaking, 40 reading, 10 writing.
- `correct` must point to a filled option. Two options in one question cannot be identical.
- Save as **CSV UTF-8** from Excel or Google Sheets.
- If anything is wrong, nothing is changed and the app lists the problems by row number.
- Tests already taken keep the questions they were answered with.

Example rows

```csv
section,question,option_a,option_b,option_c,option_d,correct,audio_text,passage,keywords
listening,What time does the bus leave?,7:15,7:45,8:15,,B,The school bus leaves at quarter to eight.,,
reading,Who wrote the note?,Mina,Ravi,Sam,,A,,"Note: Meet me at 5. - Mina",
speaking,What is your favourite subject and why?,,,,,,,,subject;science;maths;english;like;because
writing,Write 3 lines about your school.,,,,,,,,
```

Speaking `keywords` are used only for the free automatic marking. A good answer should contain at least one of them. Include different ways a student might answer.
