# Topic 1 Short Answer Studio

A standalone, browser-only practice activity for the IoT Ecosystem teaching deck. There are 15 graphic-led questions. The completion target is **12 correct answers out of 15 (80%)**.

## Student flow

1. Read the question and look at its graphic.
2. Enter one concept name or a short phrase.
3. Submit the answer.
4. A correct answer counts toward the target. An unsuccessful answer gets a hint, without a model answer.
5. Revise and resubmit, or leave the question for later.
6. Open the score overview to see correct, unsuccessful and unanswered questions.
7. Retry remaining questions. Correct answers remain counted and locked. A fresh round clears the score only after confirmation.

Question 1 uses a minimal question-and-thumbnail layout. Large introductory content is hidden while answering. Longer teaching diagrams remain available on the other questions where they help explain the scenario.

## Checking and spelling

The checker accepts specified concept names and aliases. It normalises case, punctuation, simple answer prefixes and a following “because” explanation. It tolerates small spelling changes and letter transpositions when the intended term is clear, but does not treat another recognised IoT concept as a typo.

The text field also enables the browser’s native English spellchecking. Browser suggestions depend on the browser and its dictionaries. There is no grammar grade or external AI service. Unusual correct phrasing may require an additional alias in `questions.js`.

The answer bank is appropriate for low-stakes practice. It is part of the browser source and is not a secure examination system. The checker is deliberately bounded; it does not evaluate arbitrary essays or replace a teacher’s judgement.

## Topics and source slides

| Question | Concept assessed | Source slides |
| --- | --- | --- |
| 1 | Device as an ecosystem building block | 5, 9 |
| 2 | Sensing | 7, 9 |
| 3 | Acting | 7, 8 |
| 4 | Gateway | 5, 11 |
| 5 | Platform | 5, 13 |
| 6 | Edge computing | 12 |
| 7 | Aggregation | 10 |
| 8 | Validation | 10 |
| 9 | Sorting | 10 |
| 10 | Volume | 16–18 |
| 11 | Variety | 17–18 |
| 12 | Velocity | 17–18 |
| 13 | Veracity | 17–18 |
| 14 | Value | 17–18 |
| 15 | Energy constraint | 7 |

The source is the supplied Topic 1 IoT Ecosystem teaching deck. Graphics are original teaching diagrams, plus the classroom illustration created for the companion lab. All numerical scenarios are illustrative.

## Run and publish

Open `index.html` in a modern browser, or serve this folder with `python3 -m http.server 4173`. No build, backend, account, API key or package installation is needed.

The deployed version sits at `/practice/` inside the classroom lab repository. To deploy this standalone folder instead, upload its contents to a GitHub Pages publishing root. Adjust the “Explore the classroom lab” link if the lab is hosted at another URL.

## Progress and accessibility

Answers, attempt counts, hints and scores are saved in local browser storage on the same device. They are not sent to a teacher or server. If local storage is unavailable, the activity works for the current session. Progress does not follow students to another browser or device.

Controls use native buttons and a labelled text area. Each question graphic has descriptive alternative text. Feedback uses an accessible live region. Students can pause graphics, and reduced-motion preferences are respected. There is no retry penalty.

## Edit

- `questions.js`: scenarios, graphics, accepted terms and progressive hints.
- `practice.js`: bounded answer checking, local progress, retries and completion.
- `practice.css`: focused layout, graphics and responsive styles.
- `index.html`: interface structure.
