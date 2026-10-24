---
name: xxd-panel-001
description: "XXD Panel 001｜Retro Whimsy Journal: redraws the most recognisable subject of a photo as a light, slightly clumsy, witty retro hand-drawn editorial illustration — simplified shapes with gently exaggerated proportions, thin wobbly lines, mixed watercolour, gouache, coloured pencil and pastel on grainy paper, a soft palette taken from the photo, generous cream whitespace and an optional retro handwritten title, number or year. Outputs PNG top-bottom or left-right comparisons, design-only images, or phone/tablet/desktop/watch wallpapers, from one photo or a folder. Use when the user invokes xxd-panel-001 or asks for retro hand-drawn, naive, paper-textured editorial illustration from a photo."
---

# XXD Panel 001

Create finished PNG artwork from the current user-supplied photograph or image directory. Read `references/original-prompt/zh-CN.md` completely immediately before every generation. That Chinese source brief is the sole creative and aesthetic authority; never summarise, translate, blend, or replace it with this file, a README, a sample, or another Panel.

Read `references/soldier-runtime.md` completely immediately before building every generation request. It is the sole family runtime contract for parameters, preference reuse, directory batches, preflight, prompt assembly, bitmap execution, output isolation, and acceptance. This Skill must not write a second art direction or a second runtime.

Write every selected final PNG directly inside one fresh task directory under `~/Desktop/xxd/xxd-panel-001/` (or the explicit `--out` root). Use collision-safe filenames; do not create source, mode, or size subdirectories and do not generate an automatic contact sheet.

## References

- `references/soldier-runtime.md` — family runtime contract used at generation time
- `references/original-prompt/zh-CN.md` — canonical source brief used at runtime
- `references/original-prompt/README.md` — translation index and authority note
- `references/runtime-preferences.md` — safe delivery-preference reuse
- `references/sample-workflow.md` — sample-artwork maintenance only; never a runtime prerequisite
- `references/xxd-panel-001-prompt.zh-CN.md` and `.en.md` — delivery adapter notes matching the family runtime blocks
