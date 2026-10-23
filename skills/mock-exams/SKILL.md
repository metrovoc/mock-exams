---
name: mock-exams
description: Build mock exams that replicate a course's upcoming exam in its own medium (paper, browser, media, hands-on or oral), with answer keys, from all of the course's materials.
argument-hint: "[course] [exam] [number of mocks]"
disable-model-invocation: true
---

# Mock exams

Let the student sit the exam before it happens: build mocks indistinguishable from the real exam, each with a key for self-grading.

## Guiding principle (highest priority)

Infer the instructor's intent — what they are likely to test, in what format and medium, and in what style — from the course materials. All rules below are subordinate to this principle.

## Evidence

- Work on the course the user names, otherwise the one the current directory belongs to, and on the exam they name, otherwise its next one.
- Survey ALL of the course's materials from every available source — syllabus, slides and notes, recordings, homework and its feedback, quizzes, practice and past exams, announcements, anything accessible — including anything released for the exam itself, such as readings, cases, datasets or candidate questions.
- Evidence is what comes from the course itself: the instructor's and staff's materials, and the student's record of the course, such as notes and graded work. Anything made from these afterwards for study, such as summaries, explainers, generated answers and earlier mocks, is not evidence; at best it echoes them. Never read previously generated mocks.
- Study live platforms without starting or submitting anything: opening a real quiz can use up an attempt.

## The mocks

- Build 2 mocks unless the user asks for another number. Each is one complete exam; do not organize mocks by topic.
- Replicate the real exam as faithfully as possible: content, difficulty, length, language, format, layout, medium and behavior alike.
- Question types: stay within the range the instructor would plausibly use; within it, vary composition across mocks rather than following a fixed template.
- Include only problems highly likely to appear, and within that predicted set, aim for exhaustive coverage across the mocks. Skip anything out of scope, obscure or unlikely to be tested.
- Past problems show style. Write new ones unless the instructor demonstrably reuses problems.
- Model the wording on the instructor's, and make every problem clear and unambiguous.

## Medium

Deliver each part of a mock in the medium the student will meet, using whatever tools and services reproduce it best.

- **Paper**: a print-ready PDF reproducing the real paper's cover, instructions, typography, layout, answer spaces and provided sheets.
- **Browser** (LMS quizzes, proctoring browsers, online forms): a self-contained HTML page reproducing the platform's question types, navigation, timer and restrictions, scored on submission.
- **Media** (video, audio, images): from the course, from elsewhere or generated, whichever serves the exam best.
- **Hands-on** (code, data, spreadsheets, software): the files, data and environment the exam provides, with checks that grade the work.
- **Oral**: the examiner's questions, likely follow-ups and a rubric, or a live examination by the agent.
- **Anything else**, such as a physical lab: the closest feasible substitute, noted in the key.

Every deliverable must work as delivered, and every question about a clip, image or recording must be answerable from it as delivered.

## Answer keys

For every problem: the final answer, a concise explanation, the points the real exam would award, and a one-line source note where applicable; a rubric where grading takes judgment. Each mock has its own key, out of sight until that mock is done. Begin each key with a few lines on what the prediction rests on and what had to be assumed.

## Output

- Write to the folder the user or the workspace's agent instructions name, otherwise a `mocks/` folder beside the course's folder. Other runs may work there at the same time: touch nothing in it but the workspace you create or are assigned, not even to list it.
- Create a new workspace named with a short course code and 4 random hex digits, such as `econ201-7f3a`.
- Keep the workspace under Git and commit every change, from the first build to later fixes and updates, so each can be audited.
- Name every deliverable with the workspace name and mock number, such as `econ201-7f3a-M1.pdf` and `econ201-7f3a-M1-key.pdf`.
- Mark each mock with its workspace name and number, such as `econ201-7f3a/M1`, unobtrusively and clear of the real layout's own elements, such as a footer corner on paper. This mark is the only place the mock's identity appears.
