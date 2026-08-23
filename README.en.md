<p align="center">
  <img src="./assets/banner.svg" alt="XXD Panel 001 project banner" width="1200">
</p>

<div align="center">

# 🦁 XXD Panel 001

### Translate a photograph into light, naïve, paper-breathing retro editorial illustration

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-000000?style=flat-square)](./SKILL.md)
[![Four Modes](https://img.shields.io/badge/Modes-4-d75d32?style=flat-square)](#four-outputs-one-hand-drawn-logic)
[![Raster Output](https://img.shields.io/badge/Output-PNG-3c6f67?style=flat-square)](#boundaries-and-trust)

<a href="README.md">简体中文</a> · <strong>English</strong> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.ar.md">العربية</a>

</div>

> NAÏVE LINE · RETRO PAPER · MIXED MEDIA · WITTY METAPHOR · WARM SPACE

XXD Panel 001 is an image-generation Skill for Codex and compatible agents. It preserves recognisable subjects, gestures, and relationships, then translates them into light retro editorial illustration: slightly fallible fine lines, watercolour and gouache shapes, coloured pencil, pastel or crayon, all resting on warm fibrous paper.

The result does not trace the photograph's surface. It finds one intelligent, playful, source-bound transformation and combines modernist editorial drawing, Bauhaus order, picture-book warmth, and the ease of a fashion sketch. Type feels like a restrained note left by the illustrator, not an advertising headline pasted on later.

## Why it exists

“Hand-drawn style” easily collapses into generic cute cartooning: perfectly smooth outlines, an interchangeable palette, or a digital noise filter pretending to be paper and pigment.

001 reverses that logic:

```text
lock source facts → find one source-specific visual metaphor → simplify with relaxed imperfect line → layer watercolour, gouache, pencil, and pastel → preserve warm-paper breathing room → add restrained retro lettering
```

If an unrelated photograph could replace the source without materially changing the subject, metaphor, gesture, palette, or copy, the result is not 001.

## The 001 visual contract

- **Recognisable simplified subject:** retain at least three source-specific identity cues. Proportions may be gently exaggerated, but people, objects, and relationships cannot become generic symbols.
- **Source-specific transformation:** derive one intelligent, natural visual metaphor from an action, structure, setting, or mood instead of applying a fixed visual trick.
- **Humanly imperfect fine line:** keep contours thin, relaxed, slightly wavering, broken, and breathable—never smooth vector outlines.
- **Light mixed-media depth:** combine transparent watercolour blooms, matte gouache, coloured-pencil hatching, pastel or crayon grain, and dry brush without becoming heavy.
- **Source-derived limited palette:** use high-value, low-to-medium saturation colour grounded in the photograph, with only one small complementary accent.
- **Warm paper and print imperfection:** show fibre, rough edges, slight show-through, and gentle misregistration as material evidence rather than uniform digital noise.
- **Restrained retro lettering:** keep copy short, slightly uneven, and ink-absorbed; compose it with the lines and colour fields.

## Samples · Coming soon

The repository reserves [`assets/examples/`](assets/examples/) for future work. Only finished 001 artwork verified by the project owner will be added; no post or image from another style is used as a placeholder.

Future samples will demonstrate 001's adaptability. Their subjects, metaphors, palette, copy, and canvas ratios will never become generation references or defaults.

## Four outputs, one hand-drawn logic

The four modes support single or multiple selection. Reply with `1`, `1+3`, `1,2,4`, or `all`; the Skill deduplicates and runs them in menu order 1→4. Every mode is delivered independently in its own task directory—never as an overview—and `all` yields seven PNGs per source (one for each ordinary mode plus four wallpapers). Sizes may be labelled by mode in the same reply; unlabeled ordinary modes remain source-adaptive. Copy is shared across selected modes by default and may be overridden per mode.

| Mode | Sizing logic | Deliverable |
| --- | --- | --- |
| `top-bottom` | source-adaptive | complete source above, 001 retro hand-drawn editorial illustration below; both panels retain the source size and split exactly 50/50 |
| `left-right` | source-adaptive | complete source left, 001 retro hand-drawn editorial illustration right; both panels retain the source size and split exactly 50/50 |
| `design-only` | source-adaptive | transformed design only, with no visible source photo; retains source ratio and dimensions |
| `wallpaper-pack` | four device sizes | separate phone, iPad, desktop, and children's-watch PNGs |

Exact user pixels > explicit ratio or destination > source adaptation for ordinary modes. The original `001.md` used a 3:4 creative canvas, but that historical example is not a silent default in the current Skill.

Photography in paired modes stays truthful, with only restrained grading and necessary environmental extension. Design-only and wallpapers still use the photograph as evidence but do not show it.

### Wallpaper packs: linked or independent

Wallpaper mode has no silent size default. Choose the common preset—phone `1440×3200`, iPad `2048×2732`, desktop `3840×2160`, watch `1024×1024`—or give labelled custom sizes.

- **Linked pack (recommended):** generate and approve the iPad anchor first; every other device references the original photo plus that same anchor and is recomposed for its canvas.
- **Independent set:** every device references only the source photograph and may explore different drawn simplifications, metaphors, whitespace, and copy relationships.

Linked never means cropped. All four files are separately generated, composed, and reviewed, with no iPad→phone→desktop→watch reference chain.

## Copy must feel written into the drawing

Before generation, choose automatic copy, custom copy, or text-free output. Name the target language or locale whenever copy is present.

Automatic copy distils one short title from subject identity, known place, visible atmosphere, or a symbol supported by the photograph. It may be warm and poetic, but does not force a pun, reversal, or standardised “moment of recognition”.

The default is one title. Add zero to two short annotations only when they carry real information; never invent catalogue numbers, years, coordinates, or archival labels merely to look sophisticated. Copy must still pass the unrelated-image swap test.

Finished user wording stays verbatim. A direction or editable draft is refined only while preserving audience, purpose, mandatory words, tone, and implication.

Language follows the intended audience rather than the command language:

```text
target market or audience > requested output language > direction language; if none is explicit, ask before generation
```

A Japanese edition uses natural Japanese, a Korean-audience edition uses natural Korean and correct spacing, a UK edition uses British English, and Arabic defaults to natural Modern Standard Arabic with genuine right-to-left composition. The Skill never guesses nationality from appearance, clothing, scenery, or signs and never uses pseudo-foreign text.

## Code guarantees geometry; image generation creates the artwork

The image model creates the simplified subject, imperfect line, mixed media, paper grain, source-specific metaphor, whitespace, and type. `scripts/compose_panel.py` only plans canvases, performs exact 50/50 raster composition, finalises dimensions, and audits results. It never fakes artwork with programmatic drawing.

```bash
python3 scripts/compose_panel.py --plan --layout top-bottom --source photo.png
python3 scripts/compose_panel.py --plan --layout left-right --size 2560x1440
python3 scripts/compose_panel.py --audit result.png --layout design-only --size 2048x2048
```

Exact top-bottom canvases need an even total height; left-right canvases need an even total width. Requested pixels are never silently changed.

## Get started

```bash
git clone https://github.com/nevertoday/xxd-panel-001.git
mkdir -p ~/.codex/skills
ln -s "$(pwd)/xxd-panel-001" ~/.codex/skills/xxd-panel-001
```

Claude Code users may link the same directory to `~/.claude/skills/xxd-panel-001`. Restart the agent session after installation.

```text
$xxd-panel-001
Turn this photograph into a left-right composition. Derive the copy from the image and write it in natural Korean.
```

You may invoke the Skill with only a photograph. It first asks for one or more modes in a numbered multiline menu, then for copy settings; wallpaper mode also asks for linked/independent continuity and device sizes.

Full specifications:

- [Skill workflow](SKILL.md)
- [Chinese full prompt](references/xxd-panel-001-prompt.zh-CN.md)
- [English full prompt](references/xxd-panel-001-prompt.en.md)
- [Original style brief](references/001-source.md)

## Boundaries and trust

- Each photograph stays within its own task and never borrows subjects, colours, copy, or composition from other inputs, old results, or samples.
- Every invocation creates a fresh task directory; even identical sources and parameters must generate anew.
- Deliverables are PNG bitmaps, never SVG, HTML, Canvas, or programmatic-drawing substitutes.
- The configured bitmap bridge emits sanitised status only and does not expose providers, endpoints, headers, credentials, prompts, or response bodies.
- Each selected ordinary mode returns one file; selected `wallpaper-pack` adds four separate wallpapers. `all` returns seven PNGs per source across four sibling mode directories, never a contact sheet or overview.

Local composition needs Python 3 and Pillow. The safe bitmap bridge uses Python 3.11+ `tomllib`. Image generation still requires a host agent with built-in raster generation or an already configured compatible raster route.

## Repository

```text
xxd-panel-001/
├── SKILL.md
├── README.md / README.en.md / README.ja.md / README.ko.md / README.ar.md
├── agents/openai.yaml
├── assets/
│   ├── banner.svg
│   └── examples/ (reserved for future local samples)
├── scripts/
│   ├── compose_panel.py
│   └── configured_imagegen.py
└── references/
    ├── xxd-panel-001-prompt.zh-CN.md
    ├── xxd-panel-001-prompt.en.md
    └── 001-source.md
```

## About XXD

XXD is the abbreviated brand name of Xiaoxiaodong. This project is created and maintained by [@xiaoxiaodong01](https://x.com/xiaoxiaodong01).

## Support and Membership

### In-depth Consultation · CNY 299/hour

One-to-one consultation for using the Skills is billed at CNY 299 per hour. Contact Xiaoxiaodong through the WeChat QR code below to book.

### Xiaoxiaodong Skills User Community · CNY 99 to join

A one-time CNY 99 fee joins the community for workflow sharing, work discussion, and peer support. It does not include hourly one-to-one consultation. Include “Skills User Community” in your WeChat message.

### Knowledge Planet + Member Prompt Library · CNY 699/year

[Knowledge Planet](https://wx.zsxq.com/group/15554814142882) and the [XXD Member Prompt Library](https://vip.xiaoxiaodong.ai/) are one membership: **one annual payment unlocks both, with no second purchase required.**

1. Subscribe through [Knowledge Planet](https://wx.zsxq.com/group/15554814142882), then contact Xiaoxiaodong on WeChat for a Prompt Library redemption code.
2. Subscribe through the [Member Prompt Library](https://vip.xiaoxiaodong.ai/), then contact Xiaoxiaodong on WeChat for a Knowledge Planet invitation.

<p align="center">
  <a href="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png"><img src="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png" alt="XXD paid community WeChat QR code" width="320"></a>
</p>

<div align="center">

**Keep the person and the moment recognisable; let one easy-looking drawn gesture say them more precisely.**

</div>

---

<div align="center">
  <h2>☕ Support this open-source project</h2>
  <p>If this project saved you time, a Star, a share, or a coffee helps keep it moving.</p>
  <table>
    <tr>
      <td align="center" width="240">
        <a href="https://github.com/nevertoday/zhongguo-traditional-colors/blob/main/docs/images/buy-me-a-coffee-qr.png?raw=true"><img src="https://github.com/nevertoday/zhongguo-traditional-colors/blob/main/docs/images/buy-me-a-coffee-qr.png?raw=true" alt="Support Xiaoxiaodong through Buy Me a Coffee" width="180"></a><br>
        <strong>Buy me a coffee</strong><br>
        <sub>Scan or open the QR code to support Xiaoxiaodong</sub>
      </td>
    </tr>
  </table>
  <p><sub>Support is entirely optional and never changes access to this open-source project.</sub></p>
</div>
