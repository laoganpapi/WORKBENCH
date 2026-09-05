# Three Agent Workflows for Phi Phung

Leap GeeBee Vietnam · Business Development · 5 September 2026 · Draft for discussion

The three workflows chosen from the brainstorm, numbered as there: the weekly HQ report (1), call notes into the CRM (3), and the weekly rep pipeline audit (4). One rule governs all three: the agent drafts, Phi Phung approves. Nothing reaches HQ, a partner, or the CRM without her approval; each workflow names its approval step, or says why none is needed.

Current-state statements rest on her own account of where the week goes (prospecting, follow-ups, reporting) and on assumptions marked as such. The open questions at the end list what must be confirmed before building.

## Shared Plumbing

All three workflows read the same pipeline data and use the same connectors, so build this once.

| Piece | Choice | Why |
|---|---|---|
| Pipeline data | A weekly export from the CRM, Sunday evening, into one Google Sheet, `BD Pipeline` | The agent reads Sheets today. A manual export is acceptable at the start; question 1 asks whether the CRM can schedule it. A direct CRM connection is a later upgrade. |
| History | Each weekly export kept as its own dated tab | The report and the audit compare this week's tab with last week's; that needs retained tabs. The audit's four-week comparison fills in as tabs accumulate. |
| Columns | Partner, rep, stage, stage entry date, last activity date, next step, next step date, last referral date, referrals this period, expected value | What the checks below read, together with the `Targets` tab and the `Agent` tab. |
| Targets | A `Targets` tab: the period's targets for the team and for each rep | Read by the report (team) and the audit (per rep). |
| Stale deal | No activity for more than an agreed number of days, proposed at 14; she sets the final value | One definition, used by the report and the audit. |
| Runner | Claude Code with the Gmail, Drive, and Calendar connectors | Workflows 1 and 4 run as scheduled routines; workflow 3 runs only when she or a rep pastes material in. |
| Chat channels | Zalo and WhatsApp have no connector today | The agent writes paste-ready text; she or the rep sends it from a phone. |
| Writes | Gmail drafts, Drive docs, calendar holds, and an `Agent` tab in the sheet | The agent never sends a message and never edits a CRM record in the first version. |
| `Agent` tab | One row per proposed CRM update. Columns: partner, rep, stage, next step, next step date, summary, created (date, written by the agent), status (Pending, written by the agent; Approved, set by her), approved (date, entered by her), follow-up sent (date, entered by whoever sends it) | The approval gate for workflow 3, the source of its measures, and the wins-and-risks feed for workflow 1. |
| Report template | One Drive doc, created at build time from her latest sent report | When HQ changes the format, this doc changes, not the workflow. |

## 1. The Weekly HQ Report

By her account, reporting to India is one of the three biggest drains on her week.

- **Trigger.** Monday 07:00 Vietnam time, after the Sunday export and before her week starts.
- **Reads.** This week's and last week's dated tabs; the `Targets` tab; the report template; her calendar; the week's rows in the `Agent` tab, once workflow 3 is live. Until then she supplies the wins and risks in three lines each.
- **Does.** Diffs the two tabs: new partners, stage moves, stale deals (Shared Plumbing definition), lost. Fills the KPI block HQ expects, assumed to be activations, referrals, conversions, and pipeline value, each against the team target (confirm the block with question 2). Lists the week's events and partner visits from her calendar. Pulls three wins and three risks from the `Agent` tab summaries. Writes the report in the template.
- **Delivers.** A Gmail draft addressed to the HQ recipients (question 2), and a copy in Drive. Every number carries the tab and rows it came from. Anything the columns cannot support is marked "missing", never estimated.
- **Approval.** Nothing is sent until she sends the draft. Fifteen minutes: correct the commentary, send.
- **Measure.** Time from Monday 07:00 to the Gmail sent time (target under 30 minutes).
- **To build it.** Her last four sent reports: the latest becomes the template, all four confirm the KPI definitions. The team targets. One to two days.

## 3. Call Notes into the CRM

Assumption, to confirm with her: meeting notes and Zalo threads sit in phones and notebooks, so the CRM lags days behind and follow-ups slip.

- **Trigger.** On demand: she or a rep pastes notes, a Zalo thread, or a voice-memo transcript into the agent.
- **Reads.** The latest dated tab, to match the partner.
- **Does.** Extracts partner, people, what was discussed, commitments on each side, objections, and the next step with its date, each tied to the line it came from. Matches the partner to a pipeline row and asks when the match is unsure. Writes a Pending row to the `Agent` tab: partner, rep, proposed stage, next step, next step date, a three-line summary, and the created date. Drafts the follow-up as a Gmail draft or as Zalo text, restating the commitments and confirming the next date. Places a calendar hold for the next step.
- **Delivers.** Pending row, follow-up draft, calendar hold, within minutes of the paste.
- **Rules.** Never invents a commitment. Writes the follow-up in the language of the input. Where the notes contradict the pipeline row, says so in the summary instead of choosing silently.
- **Approval.** She sets the row's status to Approved and enters the date. Only Approved rows are copied into the CRM, by the rep, since the agent does not write there in the first version. Once the row is Approved, she or the rep sends the follow-up and enters the sent date; nothing is sent to a partner before that.
- **Measure.** Share of rows approved on the created date or the next working day. Share of follow-ups sent on the approved date or the next working day. Both from the dates in the `Agent` tab.
- **To build it.** Ten sample notes and threads, the CRM field list, three follow-ups in her own words for tone. One day.

## 4. The Weekly Rep Pipeline Audit

Assumption, to confirm with her: stale deals and missing next steps surface during the 1:1, or not at all.

- **Trigger.** Sunday evening after the export, for every rep, plus a team summary. If the 1:1s sit on her calendar, each rep's page is refreshed two hours before that rep's 1:1 (question 3).
- **Reads.** The latest dated tab, the prior weeks' tabs, and the `Targets` tab.
- **Checks, per rep.** Proposed thresholds; she sets the final values.

| Check | Proposed threshold | Read from |
|---|---|---|
| Stale deals | Shared Plumbing definition, proposed 14 days | last activity date |
| Deals with no next step, or a next-step date in the past | any | next step, next step date |
| Deals too old for their stage | for example, proposal over 30 days | stage, stage entry date |
| Forecast against the rep's target | gap in value and count | expected value, `Targets` tab |
| Partners with no recent referral | over 60 days, proposed as the churn warning | last referral date |
| Deals touched this week | against the rep's prior four weeks; available once four weekly tabs exist | last activity date, across the dated tabs |

- **Delivers.** One page per rep in Drive: a scorecard, the five items to discuss, three questions to ask, suggested actions. One team page for her, with the change since last week's tab.
- **Rules.** Describes, never judges; each page is written so the rep could read it. Once agreed, the thresholds stay fixed week to week; changing them is her call, not the agent's.
- **Approval.** None needed: the pages stay inside the team and touch neither HQ, a partner, nor the CRM. Five minutes of reading before the 1:1.
- **Measure.** Count of stale deals, week on week. Share of deals with a next step and a future next-step date (target above 90 percent).
- **To build it.** Rep list, stage definitions, agreed thresholds, per-rep targets. One day, once the sheet exists.

## Order and Risks

Build in the order 1, 4, 3: the report and the audit draw on the sheet and on material she already holds, while the notes workflow also needs sample notes from reps. Three weeks end to end, one workflow live per week.

- **Export discipline.** If the export lapses, every workflow reads stale data. Schedule it if the CRM allows (question 1); otherwise name an owner.
- **Gaming.** A rep can refresh "last activity" without doing anything. The audit reads next-step quality, not activity alone.
- **HQ format changes.** Handled by the report template doc in Shared Plumbing.

## Open Questions for Phi Phung

1. Which CRM, and can it schedule a weekly export to a sheet?
2. What does HQ's report look like today, which KPIs does it carry, and who receives it?
3. How many reps, and are the 1:1s on her calendar?
4. Which notes and threads can she share as samples?

*Draft for discussion. Nothing here is built; effort estimates are unverified until the answers above are in.*
