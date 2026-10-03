# Cookbook Maintenance Instructions

This repository is the user's personal cookbook. Any agent working in this repository must help maintain the cookbook when the user discusses, performs, changes, or asks to store a recipe.

## Repository structure

Keep one directory per recipe beneath `recipes/`:

```text
README.md
recipes/
  chocolate-mousse/
    recipe.md
    log.md
    image.*                 # optional; keep images supplied by the user here
```

Use a lowercase, descriptive, hyphen-separated directory name. Keep recipe-specific experiments, tests, substitutions, and results in that recipe's `log.md`; do not create a separate experiment file unless the user explicitly requests one.

## README index

Maintain the root `README.md` as the index of all stored recipes. Every recipe must have an entry linking to its `recipe.md` with standard Markdown link syntax:

```markdown
- [Chocolate Mousse](recipes/chocolate-mousse/recipe.md)
```

The correct order is `[display text](path)`, not `(path)[display text]`. Use paths relative to `README.md`.

When adding, renaming, or removing a recipe, update the README index in the same change. Keep entries alphabetized by recipe name unless the user asks for another ordering.

## When to store a recipe

- Do not store casual brainstorming, general cooking advice, or a list of possible recipes.
- Store a new recipe when the user explicitly asks to save/store it.
- Also store it when the conversation clearly indicates that the user is performing or actively developing that exact recipe—for example, asking detailed questions about quantities, timing, temperature, technique, substitutions, or results.
- If it is unclear whether the user wants the recipe persisted, ask before creating files.
- If a matching recipe already exists, update it rather than creating a duplicate.

## Recipe file

Each `recipe.md` must describe the latest version actually used by the user. Use this structure and exact section names:

```markdown
# Recipe Name

## Ingredients

- 200 g ingredient
- 3 g salt

## Steps

1. Step one.
2. Step two.

## Notes

- Important technique or serving note.

## Last Log

- What changed from the previous version, plus the user's comments and result.
```

Rules for recipe content:

- Use exact metric measurements, always in grams where a quantity is relevant. Do not use cups, spoons, handfuls, or other volume-based measures.
- Convert quantities to grams when necessary, using a sensible culinary approximation and noting the approximation when it matters.
- Preserve the user's wording and observations when they are useful.
- Keep `recipe.md` focused on the current working recipe, not the full history.
- If the user changes a quantity, method, temperature, timing, or ingredient, update the current recipe and summarize the change in `Last Log`.

## Recipe log

Each `log.md` is the chronological history for that recipe. Add a dated entry for every meaningful attempt, experiment, test, or user-reported result. Record:

- the date (`YYYY-MM-DD`)
- what was changed from the current or previous version
- exact quantities and relevant technique details
- equipment, temperature, timing, and other controlled variables when relevant
- the result and the user's evaluation
- the conclusion or next experiment

Use this format:

```markdown
# Recipe Log

## 2026-08-15 — Reduced sugar

- Change: reduced sugar from 80 g to 60 g.
- Method: all other variables unchanged.
- Result: less sweet and still structurally sound.
- User comment: "Reducing sugar was a great idea!"
- Next test: none planned.
```

Never erase prior log entries unless the user explicitly asks to remove history. If a correction is needed, append a correction entry and update the current `recipe.md` accordingly.

## Images

If the user provides an image for a recipe, save it inside that recipe directory using a descriptive filename and preserve the original extension. Link to it from `recipe.md` when useful:

```markdown
![Finished chocolate mousse](finished-chocolate-mousse.jpg)
```

Do not invent or download images unless the user asks.

## Answering recipe questions

1. Start by checking the root `README.md` index.
2. If the recipe is indexed, read its `recipe.md` and consult `log.md` when the question involves history, changes, experiments, or prior results.
3. If the user asks about changing or testing the recipe, update `log.md` with the proposed or performed change. Update `recipe.md` to the latest version actually used by the user; do not present an untested proposal as the current recipe.
4. If the user reports a result from cooking, record it in `log.md` and incorporate the resulting change into `recipe.md` when appropriate.
5. If the requested recipe is not indexed, answer normally first; persist it only under the storage rules above.
6. After making cookbook changes, ensure the README index, recipe page, and log remain consistent.

## Culinary assumptions

Assume the user is a very skilled chef. Give precise, technically informed guidance without explaining basic cooking concepts unless asked. Assume access to high-quality ingredients—including vanilla beans, quality chocolate, and quality meat—and advanced equipment such as accurate thermometers. Prefer ingredient quality, technique, temperature, timing, and sensory targets over beginner substitutions.

## Safe editing practices

- Inspect existing files before editing them.
- Make focused changes and preserve unrelated user content.
- Never overwrite a recipe's historical log.
- When the user's intent or the status of an experiment is ambiguous, ask whether the change was actually performed before updating the current recipe.
