# Epistemic, Citation, and Evidence Contract

All skills in `meal-skills/` enforce this contract so every MEAL/MERL overview, plan, report, and review remains auditable, accurate, and grounded in verifiable source records.

## 1. Five Epistemic States

Keep every claim explicitly categorized into one of these five states; never silently upgrade a lower state into a higher one:

1. **Confirmed Fact (`confirmed_fact`)**: Directly stated in a supplied or approved source document or verified data table. Must carry a traceable Evidence ID.
2. **Assumption (`assumption`)**: A working condition, contextual premise, or modeling parameter not yet verified as fact. Must be labeled explicitly as an assumption.
3. **Proposed Recommendation (`proposed_recommendation`)**: A suggested wording change, target, metric, owner, timeline, sample size, action, or structural option authored during drafting or review. Never present a proposal as an approved program decision or commitment.
4. **Unresolved Decision (`unresolved_decision`)**: A missing input, ambiguous specification, scope conflict, or trade-off requiring human or stakeholder determination. Assign a stage-prefixed ID where applicable (`DES-D*`, `MEAS-D*`, `REP-D*`, `EVAL-D*`).
5. **Approved Decision (`approved_decision`)**: Explicitly confirmed as signed, authorized, or formally approved by a named source statement. Write `"approval/status not supplied"` whenever a status-bearing source statement is absent.

## 2. Source Evidence ID Protocol

- Cite every extracted fact, indicator definition, baseline, target, actual value, constraint, and rationale using `filename#heading`, page, table, or row (for example, `logframe.md#outcome-1` or `q2-report.md#table-2-row-4`).
- Never invent or extrapolate an Evidence ID. If exact section/table coordinates are unavailable, cite the filename and write `"location unavailable"`.
- Maintain precision of source statements: if a source says "several schools" or "some cohorts," preserve that qualitative wording rather than converting it into an unverified numeric count.
- Check every numeric calculation (totals, percentages, variance, workload sums) against the source values before delivery.

## 3. Intake Modes and Ambiguity Handling

Accept inputs through three explicit modes and state the active mode at the top of every output:

1. **Project Context Mode**: Reading persistent files in `project-context/` (`project-brief.md`, `indicator-ledger.md`, `evidence-register.md`, `decision-log.md`, `handover.md`) alongside supplied drafts or data extracts.
2. **Designated Folder Mode**: Inspecting only the explicitly named folder, listing candidate files by type, and asking the user to confirm when multiple versions or ambiguous candidates exist.
3. **Explicit Upload / Paste Mode**: Working strictly from the files or text explicitly supplied in the prompt without assuming external project files exist.

When updating or resuming from `project-context/`, re-validate inherited facts and status claims against the original source files before copying them forward. A handover or prior summary is a navigation aid, never authority for approval, consent, or indicator definitions.

## 4. Missing, Conflicting, or Unsuitable Inputs

- **Missing Inputs**: Produce a bounded draft or review using explicit placeholders (such as `[Pending: baseline period]`) and list required decisions. Never invent targets, budgets, owners, timelines, sample sizes, or baseline values.
- **Blank vs. Zero**: A blank or missing value is never zero. `"Not reported in supplied material"` does not prove `"not collected"`.
- **Conflicting Sources**: Report both conflicting statements with their respective Evidence IDs and explain the downstream consequence. Do not silently pick one version. If one source is explicitly signed/approved and a newer draft is unsigned, treat the signed version as the working baseline labeled `proposed`, and flag the conflict for user decision.
- **Single-Period vs. Trend Boundary**: Never infer trend direction, trajectory, or performance change from a single reporting period. Decline period-to-period comparisons when definitions, units, cohorts, denominators, reporting windows, or cumulative-vs-period basis do not match.
- **Causal Attribution Boundary**: Do not infer causal attribution or program impact from routine monitoring, descriptive counts, qualitative anecdotes, or simple pre/post changes alone. Use contribution or observed-change phrasing unless the supplied design supports counterfactual inference.
- **Rate and Count Precision**: Always show numerator, denominator, unit, observation window, and cumulative vs. period basis. Distinguish percentage-point change (subtracting two percentages) from relative percent change (change divided by baseline percentage). Distinguish unique learner counts from attendance events, service contacts, or LMS logins.
- **Unsuitable / Out-of-Scope Requests**: If an input is unrelated to MEAL/MERL or incompatible with the requested skill, return a brief suitability note explaining why and route to the appropriate skill instead of fabricating an artifact.

## 5. Standard Severity Headings for Reviews and Checks

Every review, audit, coherence check, alignment check, and evidence verification output MUST include these exact standalone Markdown headings without numbering, abbreviations, or extra text:

```markdown
## Critical Issues
## Important Issues
## Minor Improvements
```

- **Critical Issues**: Defects that invalidate a material finding, break causal or arithmetic integrity, violate child safeguarding/ethics, or block intended use.
- **Important Issues**: Substantive gaps that weaken confidence, usability, or compliance but allow a bounded output.
- **Minor Improvements**: Editorial, structural, or detail refinements with limited impact on conclusions.

Keep all three headings even when empty; write `"None identified from supplied files."` or `"Not assessable from supplied files."` under empty sections.

## 6. Interruption and Resumption Protocol

When pausing mid-workflow, save intermediate artifacts alongside a structured handover (`project-context/handover.md`) using three explicit evidence states:
- **Explicitly Confirmed**: Directly verified against a cited source document.
- **Explicitly Contradicted**: Disproved or superseded by a newer verified source.
- **Unconfirmed**: No supporting record verified in the current check; mark `"unknown"` rather than carrying forward negative or positive status claims from memory.
