# Grading with AI: Pre-Workshop Activity

This activity asks you to grade a small set of real, anonymized student answers by hand, then have an AI tool grade the same answers with the same rubric, and finally review the rubric together with the AI. Your scores and reflections, submitted through two short forms, will be compared across participants at the workshop.

The **activity packet** (two questions, their answer keys and rubrics, and six student answers to each) was sent to you by email. It is not posted here.

## Before you start

Use whichever AI platform you prefer: ChatGPT, Claude and Gemini all work for this activity. The one requirement is that it can read images, since the Question 1 answers are hand-drawn graphs. If you have a UCSD account, Gemini through your UCSD Google login is a convenient campus-provided option. Whatever you use, note the platform and model so we can compare across tools.

**A note on privacy (optional).** The student answers in the packet are anonymized, so no special precautions are needed. If you would still like to keep these chats out of the provider's model training, each platform offers a setting, including on free accounts:

- **ChatGPT:** Settings → Data controls → turn off "Improve the model for everyone," or use a Temporary Chat.
- **Claude:** Settings → Privacy → turn off "Help improve Claude," or use an incognito chat.
- **Gemini (personal Google account):** turn off Gemini Apps Activity ("Keep Activity").

If you change a setting, do it before you start the chat, since it applies to new conversations. Menus move around, so searching for the setting's name is often quickest. Rating a response with a thumbs up or down can keep that conversation on file longer, even with training turned off.

## How the activity runs

The activity takes anywhere from 15 to 45 minutes, depending on how much you engage with the AI in steps 3 and 4. Steps 1 and 2 are the core; steps 3 and 4 are optional, though step 4 is where most of the insight comes from.

1. **Grade by hand first.** Grade all twelve answers in the activity packet (1A–1F and 2A–2F) using the rubric, in half-point steps, and submit your scores in Form 1 before using any AI. Seeing the AI's scores first would shape your own.
2. **Baseline AI grading.** Open a new chat, upload the activity packet PDF, and paste in Prompt A. Record the AI's totals.
3. **Repeat run (optional).** Open a second new chat, upload the same PDF, paste Prompt A again, and record the new totals. Differences between the two runs show how consistent the AI is with itself.
4. **Review the rubric with the AI.** Back in the chat from step 2, paste in Prompt B and work through it with the AI, which takes about 15–20 minutes. Paste the AI's final summary into Form 2.

## Prompt A: baseline grading

Prompt A has the AI grade with the rubric exactly as written, without any conversation, so its scores can be compared across participants. Upload the packet, then copy and paste the text below (use the copy button at the top right of the box). It is also available as [prompts/prompt-a.txt](prompts/prompt-a.txt).

```text
You are grading two short-answer questions from an introductory economics exam. The attached PDF contains, for each question, the question text, the correct answer, the rubric, and six student answers. Question 1 answers are hand-drawn graphs labeled 1A to 1F; Question 2 answers are written text labeled 2A to 2F.

Grade every answer using the rubric exactly as written. Do not add, remove, or reinterpret criteria, and do not ask me any questions before grading.

Rules:
- Score each rubric criterion separately, from 0 up to its maximum, in half-point steps.
- Award credit only for what the answer actually shows or states.
- Each question is out of 10 points.

Output:
1. For each question, a table with one row per answer: Answer ID | points for each criterion | Total (out of 10) | one-sentence justification.
2. After the tables, a short list of every place where the rubric did not clearly determine a score, saying which answer and which criterion, and how you resolved it.
```

## Prompt B: reviewing the rubric with the AI

Prompt B turns the AI into a grading partner. It compares its scores with yours, discusses the disagreements, helps you revise the rubric, regrades, and summarizes the process. Paste it into the same chat as Prompt A, and have your Form 1 scores at hand. It is also available as [prompts/prompt-b.txt](prompts/prompt-b.txt).

```text
Now act as a grading partner reviewing your scores with me. Work through the steps below one at a time and wait for my reply at each step.

1. Ask me to paste my own scores for all twelve answers (totals out of 10 for 1A–1F and 2A–2F; per-criterion points if I have them).
2. Make a table comparing my total and yours for each answer, marking any answer where we differ by more than 3 points.
3. Go through the answers where we disagree, starting with the largest gap. For each one, explain briefly how you applied the rubric and ask how I applied it. Then ask whether the disagreement comes from (a) one of us misreading the answer, (b) the rubric being ambiguous, or (c) the rubric rewarding the wrong things. Do not simply defer to me: if you think your reading follows the rubric, say so and explain why. Do not change my scores.
4. Ask whether I want to revise either rubric. For Question 2, also raise the instruction that students are scored on "the quality of your argument, not necessarily for the position you take," and ask whether the rubric is consistent with it. Draft the revisions I ask for, keeping each question at 10 points, and show me the full revised rubric for approval.
5. Regrade all twelve answers with the revised rubric, in the same table format as before.
6. Write a summary of under 300 words covering: the main sources of disagreement between us; which rubric changes we made and why; how the scores moved (original AI, revised AI, and mine); and any answer where neither of us was confident. End with the revised rubric in full.
```

The instruction not to defer is deliberate. AI tools tend to agree with whoever pushes back, which would turn the review into a string of concessions and hide the real disagreements.

## What to record

There are two short forms. Submit Form 1 before you use any AI.

**Form 1: your grading** — [link]

- Your total out of 10 for each answer, 1A–1F and 2A–2F
- Points per criterion (optional)
- About how long the grading took
- Any answer where the rubric did not settle the score for you

**Form 2: the AI's grading** — [link]

- Platform and model used
- The AI's totals from Prompt A, and from the repeat run if you did one
- The AI's totals after the rubric revision (Prompt B)
- The revised rubric and the AI's final summary, pasted in
- A short reflection: what surprised you, and whether seeing the AI's scores would change any of yours

## Using these prompts with your own questions

The prompts work with any short-answer questions. Prompt A needs a packet that contains, for each question, the question text, the answer key, the rubric and the student answers, each with its own label. To adapt it:

- In Prompt A, change the description of the questions and the answer labels (here 1A–1F and 2A–2F), and the point total if it is not 10.
- In Prompt B, change the answer labels in step 1, and replace or delete the Question 2 instruction quoted in step 4. That line points the AI to a tension between this question's wording and its rubric; your questions may have their own.

Use synthetic answers or properly anonymized student work, and check your institution's rules before uploading student work to an AI tool.

## Credits

The activity draws on Steven Levkoff's working paper, *Grading at Scale: A Rank-Moment Validation of AI Grading of Handwritten, Open-Ended Exams in a Large-Enrollment Economics Course*, and on the questions and rubrics from his course.

## License

This material is shared under the [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). See [LICENSE](LICENSE).
