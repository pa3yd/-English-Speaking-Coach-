# Progress protocol

Start with canonical JSON revision and current_lesson. Empty history means no observed prior learning, not beginner failure. Missing history: ask at most one baseline prompt; do not ask the learner to repeat a long intake form.

Each item has stable id, status (unassessed/introduced/practicing/consolidating/mastered), evidence[], common_errors[], next_review_date. Evidence records session_id, date, modality (text/audio/transcript/self_report), exact user excerpt, task, support (uncued/cued/read_aloud), result and observer limitation. Record actual user errors only; never prefill plausible errors.

Introduced means taught, not learned. A correct uncued answer moves to a new task immediately. Suggested mastery criterion: independent use in two different contexts on two sessions, one being delayed retrieval; otherwise consolidating. This is an operational coaching marker, not a proficiency certificate. Mastery of wording does not imply pronunciation mastery. Self-report may be stored with its label but cannot satisfy independent mastery. Initial review suggestions: practicing next session; consolidating after 3 days; mastered after 7 days. Set a due date only after a real session; overdue reviews are not homework debt. User can adjust the interval.

Closing summary: observed success with quote; one real issue or “none observed”; exact next target. Then output complete updated JSON or a patch with base revision. Increment revision once per completed session, preserve session ids and earlier evidence, avoid duplicate session application. If no writable file exists, label proposed_progress and ask the user to retain it. Do not claim saved. Next launch reads the user's latest snapshot. If two snapshots conflict, ask which is authoritative.

No audio: pronunciation=null and pronunciation_status=not_assessed. Transcribed words alone do not establish sound quality, spontaneous pace or listening comprehension. Audio observations must cite an actual heard segment; do not score accuracy percentages or CEFR levels from a short exercise.

Local update: write to a temporary file in the same directory, parse and check it, then replace progress.json atomically. Do not change a packaged installed snapshot when canonical workspace progress is available. ChatGPT project files require manual replacement/export unless confirmed tools provide file writes; never silently maintain parallel authoritative logs.
