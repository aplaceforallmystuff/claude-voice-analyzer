# Claude Voice Analyzer

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude_Code-Skill-blue)](https://claude.ai)

A Claude Code skill for creating portable voice profiles from writing samples.

## The Problem

AI writing often sounds generic because it has no reference for your actual voice. This results in:

- Content that "could have been written by anyone"
- Loss of personality and distinctive style
- The need to heavily edit every AI output
- Readers noticing the shift from your authentic voice

This skill extracts your voice patterns and creates a reusable style guide.

## How It Works

Provide 3-5 writing samples where your voice feels strongest. The skill:

1. **Analyzes** patterns across all samples
2. **Identifies** your distinctive voice markers
3. **Generates** a VOICE.md style guide
4. **Creates** a forbidden phrases list specific to your anti-patterns
5. **Provides** testing prompts to validate the guide

## What It Analyzes

| Dimension | What It Examines |
|-----------|------------------|
| **Sentence Patterns** | Length, variation, starters, fragment usage |
| **Vocabulary** | Formality, jargon, characteristic phrases |
| **Rhythm** | Paragraph length, transitions, pacing |
| **Tone** | Humor style, directness, reader relationship |
| **Structure** | Lists vs prose, headers, formatting |
| **Opinion** | How you state views, qualify claims, express authority |

## Installation

### Option 1: Skills CLI

```bash
npx skills add aplaceforallmystuff/claude-voice-analyzer
```

### Option 2: Copy to your Claude Code skills directory

```bash
# Clone the repository
git clone https://github.com/aplaceforallmystuff/claude-voice-analyzer.git

# Copy to your Claude Code skills directory
cp -r claude-voice-analyzer/skills/voice-analyzer ~/.claude/skills/
```

### Option 3: Clone directly to skills directory

```bash
git clone https://github.com/aplaceforallmystuff/claude-voice-analyzer.git ~/.claude/skills/voice-analyzer
```

### Option 4: Manual installation

1. Create the directory: `mkdir -p ~/.claude/skills/voice-analyzer`
2. Download [SKILL.md](skills/voice-analyzer/SKILL.md) to that directory

## Usage

The skill activates when you ask Claude to:

- "Analyze my writing voice"
- "Create a voice profile from these samples"
- "Generate a VOICE.md for my writing style"
- "Help me set up voice-matched AI writing"

### Sample Selection

**Good samples:**
- Newsletter issues you're proud of
- Blog posts that felt natural
- Emails where your voice came through
- Social media threads that "felt like you"

**Avoid:**
- Heavily edited corporate content
- Collaborative pieces
- Anything that felt forced

### Output: VOICE.md

The skill generates a comprehensive style guide including:

```markdown
# Voice Profile: [Name]

## Voice Summary
[2-3 sentence description of overall voice]

## Core Characteristics
- Sentence patterns
- Vocabulary fingerprint
- Rhythm and flow
- Tone markers
- Structural habits
- Opinion expression style

## The Forbidden List
- Never use (these kill your voice)
- Use sparingly (context-dependent)
- Watch for clusters (OK alone, bad together)

## Testing Prompts
[Prompts to validate the guide works]
```

## Where to Save VOICE.md

| Location | Scope |
|----------|-------|
| `./.claude/VOICE.md` | This project only |
| `~/.claude/voice/VOICE.md` | All projects |
| `~/.claude/voice/[context]-voice.md` | Multiple profiles (professional, casual) |

## Related Skills

Part of the [aplaceforallmystuff](https://skills.sh/aplaceforallmystuff) skills collection:

- **[voice-editor](https://github.com/aplaceforallmystuff/claude-voice-editor)** — Uses the VOICE.md this skill generates to guide rewrites
- **[the-antislop](https://github.com/aplaceforallmystuff/the-antislop)** — Detect and fix AI writing patterns
- **[slop-detector](https://github.com/aplaceforallmystuff/claude-slop-detector)** — References VOICE.md for personalized pattern detection

## License

MIT License - see [LICENSE](LICENSE)

---

**The goal: Voice profiles that let AI produce content readers recognize as authentically yours.**
