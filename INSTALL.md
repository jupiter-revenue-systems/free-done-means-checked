# How to Install the done-means-checked Skill

A skill is a small instruction file Claude reads by itself when the job calls for it. This one loads before Claude tells you something is done.

Pick the Claude you use. Menus move now and then. If a name below isn't where I say, search Settings for "Skills".

## Claude.ai (web or the desktop app)

1. Find the folder `skill/done-means-checked` in this download. It has one file in it, `SKILL.md`.
2. Zip that folder. On a Mac, right-click it and choose Compress. On Windows, right-click, Send to, Compressed folder.
3. In Claude, open Settings, then Capabilities, then Skills.
4. Upload the zip and turn the skill on. If Claude asks you to turn on code execution first, turn it on. Skills need it.
5. Start a new chat and say: `Use the done-means-checked skill for everything in this chat.`

## Claude Cowork

Cowork uses the skills on your Claude account, so the steps above cover it.

A second way that always works: put this whole download in the folder Cowork is working in, then say:

```
Read skill/done-means-checked/SKILL.md and follow it for everything in this task.
```

## Claude Code

Copy the skill folder into your skills folder. This command copies. It doesn't move or delete anything.

```
mkdir -p ~/.claude/skills && cp -R skill/done-means-checked ~/.claude/skills/
```

Start a new session. Claude loads the skill before it tells you something is done, or you can type `/done-means-checked`.

To use it in one project only, copy it to `.claude/skills/` inside that project instead.

## No skills on your plan, or you use ChatGPT

Open `skill/done-means-checked/SKILL.md`. Copy everything below the top block (the part between the two `---` lines). Paste it into your project instructions or custom instructions, or as the first message of a chat.

## Check it's working

Ask: `I asked for 3 changes to my homepage. Are they done?`

A working install doesn't say yes. It asks for the 3 changes and the live link, lists each one as its own row, and tells you what it hasn't checked.
