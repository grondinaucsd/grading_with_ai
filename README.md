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
4. **Review the rubric with the AI.** Back in the chat from step 2, paste in Prompt B and work through it with the AI, which takes about 15–20 minutes. Prompt B ends with a link that opens Form 2 with all the AI's scores already filled in.

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

Prompt B turns the AI into a grading partner. It compares its scores with yours, discusses the disagreements, helps you revise the rubric, regrades, and summarizes the process. Paste it into the same chat as Prompt A, and have your Form 1 scores at hand, plus the repeat-run totals if you did step 3. At the end, the AI gives you a link that opens Form 2 with its scores filled in. Check them against the AI's tables before submitting, since the AI can make transcription slips. It is also available as [prompts/prompt-b.txt](prompts/prompt-b.txt).

```text
Now act as a grading partner reviewing your scores with me. Work through the steps below one at a time and wait for my reply at each step.

1. Ask me to paste my own scores for all twelve answers (totals out of 10 for 1A–1F and 2A–2F; per-criterion points if I have them). Also ask whether I did a repeat run of Prompt A in a separate chat, and if so, to paste its twelve totals.
2. Make a table comparing my total and yours for each answer, marking any answer where we differ by more than 3 points.
3. Go through the answers where we disagree, starting with the largest gap. For each one, explain briefly how you applied the rubric and ask how I applied it. Then ask whether the disagreement comes from (a) one of us misreading the answer, (b) the rubric being ambiguous, or (c) the rubric rewarding the wrong things. Do not simply defer to me: if you think your reading follows the rubric, say so and explain why. Do not change my scores.
4. Ask whether I want to revise either rubric. For Question 2, also raise the instruction that students are scored on "the quality of your argument, not necessarily for the position you take," and ask whether the rubric is consistent with it. Draft the revisions I ask for, keeping each question at 10 points, and show me the full revised rubric for approval.
5. Regrade all twelve answers with the revised rubric, in the same table format as before.
6. Write a summary of under 300 words covering: the main sources of disagreement between us; which rubric changes we made and why; how the scores moved (original AI, revised AI, and mine); and any answer where neither of us was confident. End with the revised rubric in full.
7. Finally, build a link that pre-fills my results form. In the template below, replace each {xx_RUN1} with your first-run total for that answer, each {xx_REVISED} with your revised total, and each {xx_REPEAT} with the repeat-run total I gave you. Write every score exactly as one of 0, 0.5, 1, 1.5, and so on up to 10, with no "/10" and no spaces. Set {DID_PROMPT_B} to Yes. If I gave you repeat-run totals, set {DID_REPEAT} to Yes; otherwise set it to No and remove each repeat placeholder, leaving nothing after its = sign. Change nothing else in the link, and show it as one clickable link.

TEMPLATE:
https://docs.google.com/forms/d/e/1FAIpQLSendhbRquiw7FsgUGBySwN-DpHuhqp5cT8URaIISonUT7Td1g/viewform?usp=pp_url&entry.370310571={1A_RUN1}&entry.1782066300={1B_RUN1}&entry.1349976808={1C_RUN1}&entry.582172106={1D_RUN1}&entry.280790732={1E_RUN1}&entry.714378158={1F_RUN1}&entry.350797686={2A_RUN1}&entry.134757090={2B_RUN1}&entry.451912898={2C_RUN1}&entry.875234232={2D_RUN1}&entry.1650685401={2E_RUN1}&entry.880601838={2F_RUN1}&entry.692126564={DID_REPEAT}&entry.878394593={1A_REPEAT}&entry.1661110712={1B_REPEAT}&entry.134749704={1C_REPEAT}&entry.1702990827={1D_REPEAT}&entry.293655989={1E_REPEAT}&entry.1513282163={1F_REPEAT}&entry.1656903180={2A_REPEAT}&entry.411155878={2B_REPEAT}&entry.535881038={2C_REPEAT}&entry.1151268204={2D_REPEAT}&entry.783493224={2E_REPEAT}&entry.2063788775={2F_REPEAT}&entry.124554294={DID_PROMPT_B}&entry.449294165={1A_REVISED}&entry.267607734={1B_REVISED}&entry.307116589={1C_REVISED}&entry.318158166={1D_REVISED}&entry.1697450955={1E_REVISED}&entry.1116156818={1F_REVISED}&entry.479561385={2A_REVISED}&entry.521784806={2B_REVISED}&entry.1069909123={2C_REVISED}&entry.1540681156={2D_REVISED}&entry.604257074={2E_REVISED}&entry.902585950={2F_REVISED}
```

The instruction not to defer is deliberate. AI tools tend to agree with whoever pushes back, which would turn the review into a string of concessions and hide the real disagreements.

## What to record

There are two short forms. Submit Form 1 before you use any AI.

**Form 1: your grading** — [open Form 1](https://docs.google.com/forms/d/1nxWAVpaYkHzenKX9qbnDvPML2Vk6s8QwLQFauYNCzB4/viewform)

- Your total out of 10 for each answer, 1A–1F and 2A–2F
- Points per criterion (optional)
- About how long the grading took
- Any answer where the rubric did not settle the score for you

**Form 2: the AI's grading** — [open Form 2](https://docs.google.com/forms/d/e/1FAIpQLSendhbRquiw7FsgUGBySwN-DpHuhqp5cT8URaIISonUT7Td1g/viewform)

If you completed Prompt B, use the link the AI gave you instead: the scores below will already be filled in, and you only add the text answers. If you stopped after Prompt A, open the form here and enter the AI's scores yourself.

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
