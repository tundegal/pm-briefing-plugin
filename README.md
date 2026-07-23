# PM Briefing Plugin

A Claude Code plugin that helps PMs write proper UX briefs before handing work to designers.

## What it does

PIP the Owl 🦉 guides your PM through 7 focused questions in a friendly, gamified conversational interview. At the end, a structured brief is printed in the terminal and a Jira ticket is created automatically.

PIP is expressive — he reacts differently depending on how the conversation is going:

```
Neutral          Happy            Celebrating
    ,___,            ,___,            ,___,
   (O v O)          (^ v ^)          (* v *)
   /)   (\          /)   (\          \)   (/
    ^ ^ ^            ^ ^ ^            ^ ^ ^
```

## Install

```bash
claude plugin marketplace add tundegal/pm-briefing-plugin
claude plugin install pm-briefing
```

## Usage

```
/pm-briefing
```

The PM runs this in Claude Code. PIP asks 7 questions, one at a time:

1. What customer problem are we solving?
2. Who experiences this problem? *(multi-select: Marketer, Admin, B2C, B2B)*
3. What should the user be able to do after this that they can't do today?
4. How will we know this worked?
5. What existing features or systems does this touch?
6. What are we explicitly NOT doing in this iteration?
7. Any examples or references to consider?

Thin answers get one gentle, context-aware follow-up. At Q4 a halfway milestone fires. At the end, a formatted brief is printed and PIP helps push it straight to Jira.

## Output

- Structured brief printed in the terminal
- Markdown block ready to paste into Confluence or Jira
- ⚠️ Quality note if any answers were vague
- Jira Task created in the UXT project with all brief fields mapped
