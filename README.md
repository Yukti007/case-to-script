# case-to-script

A Claude skill that turns a raw case into content for a creator working at the intersection of tech, curiosity and business.

You give it three lines: the problem, who has it, and what you noticed. It runs a five-step pipeline and produces a reel, caption, image cues, a LinkedIn post and a Substack outline.

It never produces explainer content ("what is X"). Every piece follows a diagnosis format:

1. A specific problem someone has
2. The obvious move, and why it disappoints
3. What is actually going on
4. The direction to look, and what it costs

## The pipeline

1. **Intake** - restates your case in one line and asks for anything missing.
2. **Research** - uses web search if available. Returns 4-5 sources with links, key numbers and the strongest counter-view. Unverified items are marked.
3. **Angles** - proposes 2-3 diagnoses. Rejects any that a generic explainer account could post. Stops and waits for you to choose.
4. **Script** - for your chosen angle: a 45-60 second reel as spoken beats, caption text, image pop-up cues, a LinkedIn post and a Substack outline.
5. **Check** - tests every factual claim against the sources, lists anything unsupported, and reminds you to rewrite the hook in your own words.

## Install

### Claude apps (claude.ai, desktop)

1. Download `case-to-script.zip` (build it yourself with the command below, or grab it from the Releases page if one is published).
2. The ZIP must have the `case-to-script` folder at the top level, so that `case-to-script/SKILL.md` is the path inside the archive.
3. Open **Settings > Capabilities** (or **Customize > Skills**), turn on Skills and code execution if prompted, then choose **Upload skill** and select the ZIP.
4. Toggle the skill on.

To build the ZIP from this repo:

```bash
zip -r case-to-script.zip case-to-script -x "case-to-script/references/voice-profile.md" "case-to-script/references/rejected-scripts.md"
```

### Claude Code

Copy the skill folder into your skills directory.

macOS / Linux:

```bash
git clone https://github.com/Yukti007/case-to-script.git
mkdir -p ~/.claude/skills
cp -r case-to-script/case-to-script ~/.claude/skills/
```

Windows (PowerShell):

```powershell
git clone https://github.com/Yukti007/case-to-script.git
New-Item -ItemType Directory -Force "$HOME\.claude\skills" | Out-Null
Copy-Item -Recurse case-to-script\case-to-script "$HOME\.claude\skills\"
```

Restart Claude Code. The skill is available as `/case-to-script`, and Claude will also load it when you describe a case.

## Make it sound like you

The skill reads two optional private files from `case-to-script/references/`:

- `voice-profile.md` - copy from `voice-profile.template.md` and fill in your style and 2-3 posts you like.
- `rejected-scripts.md` - copy from `rejected-scripts.template.md` and log scripts you rejected, with why.

If they are missing, the skill falls back to the blank templates and writes in a neutral voice. This repo's `.gitignore` keeps your private copies out of version control.

## Usage example

Paste this into Claude:

```
/case-to-script
Problem: A solo founder in Bengaluru pays for three AI tools, and her team of two still spends Mondays copy-pasting between them.
Who has it: Early-stage founders running lean teams of 1-5 people.
What I noticed: The tools each save time alone, but the hand-offs between them eat the savings.
```

Claude restates the case, researches it, and proposes 2-3 diagnoses, then stops. Reply with the angle you want (for example "Angle 2") and it writes the reel beats, caption, pop-up cues, LinkedIn post and Substack outline, followed by a claim-by-claim check.

## Files

```
case-to-script/
  SKILL.md
  references/
    format.md
    voice-profile.template.md
    rejected-scripts.template.md
```

## License

MIT. See [LICENSE](LICENSE).
