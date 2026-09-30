# resumeBuddy Skill

Tailor a resume, cover letter, or outreach message to a specific job
posting — using your own master resume, inside a Claude conversation you
already have. No API key, no account, no data leaves the conversation.

This is a companion to [resumeBuddy](https://resumebuddy.boringbydesign.com),
a free browser extension and web app for the same job — this Skill brings
the same grounded, no-fabrication tailoring approach to anyone with a
Claude subscription, with nothing to install beyond the Skill itself.

## What it does

Given your master resume and a job posting, it can generate:

- A match-confidence check (is this posting even worth applying to?)
- Tailored resume bullets
- A full tailored resume, formatted to parse cleanly through applicant
  tracking systems (ATS)
- A cover letter
- A short hiring-manager outreach message
- A spoken elevator pitch
- A third-person executive bio

Every output is grounded strictly in what's actually in your resume — it
will not invent skills, employers, or accomplishments to make you look like
a better fit.

## Install & use — Claude Code (CLI)

Clone into your local skills directory:

```
git clone https://github.com/lalcaraz/resumebuddy-skill.git
cp -r resumebuddy-skill ~/.claude/skills/resumebuddy
```

Then, in any Claude Code session, point it at files on disk:

> Use the resumebuddy skill to tailor my resume at ~/resume.pdf to this job
> posting: [paste job description]

It reads your resume straight off disk, and writes each output (e.g.
`tailored-resume.md`, `cover-letter.md`) to your working directory.

## Install & use — Claude web (claude.ai)

Skills on claude.ai are uploaded per-workspace, not cloned. Download this
repo as a zip and upload it under **Settings → Capabilities → Skills**
(requires a Pro/Max/Team/Enterprise plan — Skills aren't available on the
free tier). No local filesystem is involved:

- **Resume input:** attach your resume file to the chat message instead of
  giving a path.
- **Job posting:** paste it directly into the chat.
- **Output:** comes back as a downloadable file attached to the
  conversation (or inline text for short outputs), not written to any
  persistent disk location — download and save it yourself.

Either way, ask the same thing:

> Use the resumebuddy skill to tailor my resume to this job posting:
> [paste job description]

It will ask for whatever it's missing (resume, job description, which
output you want).

## Notes

- Your master resume and the job posting stay inside your conversation with
  Claude — nothing is sent to any third-party service by this Skill.
- Works best with a master resume as PDF, Markdown, or plain text.
- No application tracking, no resume-builder wizard — this Skill is
  generation only. For those, see the full [resumeBuddy](https://resumebuddy.boringbydesign.com)
  app.

## License

MIT — see [LICENSE](LICENSE).
