# WORKFLOW_PROTOCOL.md

# CROSS-ENVIRONMENT WORKFLOW / "갱신" PROTOCOL v1.0

**Effective:** 2026-09-04

Purpose:
Preserve project state, exact decisions, prompts, assets, execution evidence, and next actions so work can move between ChatGPT, Claude, local/manual work, and future environments without silently restarting or losing critical detail.

## 0. Trigger

When the user says **"갱신"**, run the full repository reconciliation process in this document.

"갱신" does not mean append another handoff note. It means:
1. reconcile what changed;
2. modify authoritative existing files;
3. create a new file only for a genuinely new durable artifact/authority;
4. remove or explicitly supersede contradictions;
5. update exact current state and next action;
6. commit/push;
7. verify the remote result;
8. when the AutoPipeline parent exists, update its child-repository pointer too.

## 1. Single-source-of-truth principle

Never rely on chat memory as the only copy of a durable decision.

If a clean environment would need something to continue correctly, preserve it in GitHub:
- project purpose / big flow;
- current phase;
- locked design/style/architecture;
- exact reusable prompts;
- exact asset/reference identities and paths;
- source/provenance;
- episode/experiment state;
- known failure modes;
- QC results;
- execution parameters;
- real blockers;
- exact next action.

## 2. Prefer modification over file proliferation

Do not create NEW_SESSION_HANDOFF, LATEST, FINAL_FINAL, or session-specific state files when an existing canonical file can be updated coherently.

Create a new file only if it is:
1. a new authority layer with a distinct lifecycle;
2. a reusable specification/schema/protocol;
3. an independently auditable episode/experiment/source artifact;
4. a binary/reference asset that cannot be represented losslessly in existing text.

Git history is the archive. Canonical files represent the present.

## 3. Start-of-session restore

Before substantive work:
1. identify the active repository/project;
2. read its README entrypoint;
3. read CURRENT_STATE;
4. follow the authority hierarchy from those files;
5. read the active episode/experiment package;
6. inspect recent relevant commits when needed;
7. do not re-plan from scratch if the repository already defines the state.

If another model/session changed the repo, fetch remote state again before acting.

## 4. During-work recording rule

Record durable evidence in the proper existing artifact:
- architecture decision -> architecture/lock document;
- style failure -> style/generation protocol + active episode evidence;
- exact production outcome -> episode/experiment package;
- changed next action -> CURRENT_STATE;
- changed entrypoint/authority hierarchy -> README.

Keep ephemeral reasoning out unless it changes a durable decision.

## 5. "갱신" reconciliation order

A. Decision reconciliation
- what changed;
- what remains unchanged;
- what old text is now wrong/superseded;
- new blockers;
- new verified evidence.

B. Update durable authorities first if their rules changed.

C. Update the active episode/experiment/source package with exact result, pass/fail, defects, relevant prompt/settings, and next retry condition.

D. Update CURRENT_STATE last with big flow, exact current stage, completed work, blocker/failure, and immediate next actions.

E. Update README only if entrypoint, authority order, project purpose, or canonical-file discovery changed.

F. Commit/push with clear semantic messages.

G. Verify by refetching changed files and/or latest commit. Do not say "updated" until remote state is verified.

H. When `noru358/AutoPipeline` exists:
- update child first;
- advance parent submodule pointer to the verified child commit;
- update parent cross-project state only when needed;
- push and verify parent.

## 6. Asset integrity

Text is not a lossless substitute for important visual/audio assets.

If an asset is a real authority, preserve the actual file in the repository when practical.

Do not claim an asset is preserved unless the remote path has been verified.

For large/transient outputs, preserve at minimum exact filename/ID/hash, generation settings, verdict, reason it matters, and authoritative-original location.

## 7. Generative reference rule

If visual identity depends on a reference image:
- the actual approved reference image outranks prose;
- prompts reinforce it; they do not replace it;
- a failed generated image must never become the sole style reference for the next generation;
- style reference and scene/continuity reference are separate roles;
- style reference wins on rendering language.

If the canonical visual reference is unavailable in the current environment, stop production generation rather than inventing the style from text.

## 7.5 Generic media-conditioning preflight

This project follows the parent AutoPipeline MEDIA_INPUT_CONTRACT for reference-dependent generation.

Do not hard-code TopView asset names, character names, or current episode filenames into orchestration logic.
Represent each dependency as data:
- requirement_id;
- role;
- media_type;
- source_id;
- conditioning;
- required.

The runtime/provider adapter supplies capability information and actual supplied-media evidence.

MUST_SUPPLY_MEDIA fails closed if:
- the current provider cannot accept explicit media;
- the media type is unsupported;
- the declared source was not actually supplied;
- integrity evidence fails when required.

This applies equally to visual identity, first-frame anchors, voice references, dialogue/timing audio, and future media dependencies.

## 8. Environment portability

Use repository-relative paths in canonical docs.

Do not depend on one computer's Desktop path, one chat's hidden context, one model's memory, or an unrecorded UI selection.

When environment setup matters, record tool/runtime, required version if relevant, environment variable names only, and restoration commands.

Never commit secrets or API keys.

## 9. AutoPipeline parent architecture

Target parent:
`noru358/AutoPipeline`

Use a **Git superproject + submodules**, not copied nested repositories.

Target tree:

```text
AutoPipeline/
├── README.md
├── WORKFLOW_PROTOCOL.md
├── .gitmodules
├── instatoon/   -> noru358/instatoon @ exact commit
└── talkshow/    -> noru358/talkshow @ exact commit
```

The parent records exact child commit combinations; child-specific authorities remain inside each child repository.

## 10. Definition of "lossless"

A clean environment should be able to determine what the project is, what is locked, what was tried, what failed and why, exact current state, authoritative assets/prompts, and what to do next without the previous chat transcript.

Preserve decision/state fidelity, not conversational noise.
