# MYP Vault: the answer-mark gap

**Prototype by Anvitha Abbagani. Sample questions and mark schemes written for this demo, not IB material.**

**Live:** https://mypvault.abbagani.com

MYP students know the content but lose marks turning it into answers: mark schemes assume an
examiner's eye, and general AI tools explain well but don't mark. MYP Vault grounds every answer in
mark schemes, so students see exactly which points earn marks.

**What the prototype does:**
- **Exam mode:** ask a question with its marks and get one numbered point per mark, each a marking
  point from the mark scheme, with its source. Includes a calculus question (find a derivative).
- **Evaluation mode:** answer it yourself and get an estimated score, the points hit and missed, what
  to add, and the mistake type. A better second attempt is recorded as Answer Score Improvement.
- **Explanation mode:** an analogy, plain bullets, a diagram and the exam question it links to.
- **Guardrails:** out-of-scope, coursework and full-paper requests are refused; weak matches state
  low confidence and offer the closest topics.
- **How this answer was built:** the real pipeline, run in the browser: query terms, 12 chunks
  retrieved, 6 kept after re-ranking, checks and the context budget.
- **Library:** every sample paper, one marking point per chunk. Upload your own mark scheme as a .txt
  file (one marking point per line) or add a sample one.
- **About:** runs the PRD's Appendix E test set against the pipeline.
- **Recents:** chats are kept like in a chat app; reopen or delete them from the sidebar. Each chat
  starts fresh, and every answer carries a citation chip naming its paper and question.
- Light and dark mode, and a seven-step Quick tutorial.

**What it doesn't do:** run an AI model (answers are assembled from retrieved marking points),
use real IB papers, or offer accounts, study plans or flashcards. State stays in this browser.

It is one HTML file with no build step. The only network request is for its Google Font.
