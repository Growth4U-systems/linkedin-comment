# linkedin-comment

A Claude Code skill that helps you grow on LinkedIn the way the network actually rewards: by commenting with value, not by treating your profile as a shop window.

## Why this exists

Most people use LinkedIn as a shop window. They polish their own posts, broadcast, and wait to be seen. That is the slow lane. LinkedIn is a social network, and it rewards participation.

The most underused growth lever is the comment. A good comment on someone else's post puts you in front of their whole audience, people who would never have found you on their own. You borrow their reach. The platform leans into this: comments weigh more than likes, early comments get more distribution, and real conversation spreads a post further. Commenting is also how you compound fastest when you are small.

But it only works if the comment gives value. "Great post" is noise. A comment with a real idea, a lived experience, or a sharp friendly question gets seen, earns reactions, and pulls people to your profile. That visit becomes a follower, and your own posts then reach more people. Commenting feeds posting.

## What the skill does

Three jobs, in order:
1. **Builds your list.** From your role and company, it infers your ICP and researches a focus group of real people worth engaging, split into two lanes: the people you sell to (relationships) and the big creators your audience already follows (borrowed reach). You prune the list.
2. **Chooses who to comment on.** A small core you engage every time, plus a rotating bank with a cooldown so you never feel spammy. It picks the freshest, most relevant posts each day.
3. **Writes the comments in your voice.** Like a peer, not a professor. Short, one idea, in the language of the post, with the AI tells stripped out. It leaves them ready for you to paste; it never posts for you.

The list is saved locally so future runs skip the research and go straight to commenting.

## What it does NOT do

- It does not scrape LinkedIn or automate your account. You see and post things yourself.
- It does not publish anything. Everything is left ready for you to paste.
- It needs no API keys, tokens, or paid services. It uses only standard Claude Code tools (web search and web fetch for research, plus the conversation). If web tools are not available, it works from names you provide.

## Install

### Option 1: as a plugin (recommended)

In Claude Code, run:

```
/plugin marketplace add Growth4U-systems/linkedin-comment
/plugin install linkedin-comment@linkedin-comment
```

(The part before `@` is the plugin, the part after is the marketplace; both are named `linkedin-comment`.) If your session does not pick it up right away, run `/reload-plugins`.

### Option 2: as a plain skill (no plugin system)

```
git clone https://github.com/Growth4U-systems/linkedin-comment.git
cp -r linkedin-comment/skills/linkedin-comment ~/.claude/skills/
```

Then start a session and say something like "help me grow on LinkedIn" or "who should I comment on today, here are the posts."

## How to use it

- **First run:** it builds your focus group. Have your role and company ready, and answer a couple of short questions (region, who you want to reach).
- **Every run after:** it reads your saved list, tells you who to comment on, and writes the comments. You bring the posts (paste them in), since it does not log into LinkedIn.

## License

MIT. See [LICENSE](LICENSE).
