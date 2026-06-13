---
name: linkedin-comment
description: Use this skill to grow a personal brand on LinkedIn through high-value commenting on other people's posts. Use it whenever the user wants to grow their LinkedIn presence, build authority, get more followers or profile views, figure out WHO to engage with, build a list of people to comment on, decide who to comment on today, or write comments that don't sound like AI. Trigger on phrasings like "grow on LinkedIn", "who should I follow or comment on", "build my LinkedIn audience", "get more LinkedIn followers", "engage on LinkedIn", "my LinkedIn isn't growing", "help me comment on posts", "build a focus group of people to engage", even when the user does not say the word "comment". Do NOT use this for writing the user's OWN posts (that is content creation) or for paid LinkedIn ads.
---

# LinkedIn Engagement: grow by commenting with value

Most people treat LinkedIn as a shop window: they polish their own posts, broadcast, and wait to be seen. That is the slow lane. LinkedIn is a social network, and it rewards participation, not display.

The most underused growth lever is the **comment**. A good comment on someone else's post puts you in front of their entire audience, people who would never have found you on their own. You borrow their reach. And the platform leans into this: comments weigh more than likes, early comments multiply distribution, and real back-and-forth conversation triggers the algorithm to spread the post further. Commenting is also how you compound fastest when you are small, because you are renting other people's audiences instead of waiting to build your own.

But it only works if the comment **gives value**. "Great post" is noise that no one sees. A comment that adds a real idea, a lived experience, or a sharp and friendly question gets seen, gets reactions, and pulls people to your profile. That profile visit is what turns into a follower, and your own posts then reach more people. Commenting feeds posting.

This skill helps the user do three things, in order:
1. **Build the list** of people worth engaging with (their focus group).
2. **Choose who to comment on** today, sustainably, from that list.
3. **Generate the comments** in the user's own voice, so they sound human and add value.

## What this skill does NOT do

- It does **not** scrape LinkedIn or automate the user's account. Automated activity gets accounts restricted or banned, and the account is the whole asset. The user sees posts however they normally do (open LinkedIn, scroll, or paste posts in). This skill never logs in or acts on their behalf.
- It does **not** publish anything. It prepares the list, the selection, and the comments, and leaves them ready for the user to paste themselves.
- It needs **no API keys, tokens, or paid services.** It uses only what a standard Claude Code session already has: web search and web fetch for research, and the conversation itself. If web tools are unavailable, it still works by asking the user to bring names and posts.

## How to use this skill

### Start every run here: read the list file

This skill keeps the user's focus group in a local file, `linkedin-focus-group.md`, in the working directory. It holds each person (name, profile URL, tier, lane) and a small state: the date they were last suggested for a comment, used for the cooldown in step 3.

**Your literal first action is to READ `linkedin-focus-group.md`.** Read it, do not just `ls` it. A directory listing can be stale and lie about whether the file is there; a read either returns the contents or fails cleanly because the file is absent. Then branch:

- **The user pasted in specific posts and just wants comments.** This is common, so check for it first. Skip everything else and go straight to step 4. Do not build or touch the list; they did not ask for that.
- **The file exists with a real list.** Do NOT rebuild it. Go to step 3 (choose who to comment on) and step 4 (generate the comments). Only change the list when the user explicitly asks to add, remove, or re-tier someone.
- **The file exists but clearly does not match this user** (placeholder names, or a list for a different role or region). Do not silently overwrite it; never destroy the user's data. Point out the mismatch and offer to rebuild the list with their permission.
- **The file does not exist.** Build it first (steps 1 and 2), save it to `linkedin-focus-group.md`, then continue to steps 3 and 4.

So the first run is usually "build the list, then comment." Every run after is "comment on the existing list," which is the common case. This keeps the user from re-researching people they already chose, and lets the cooldown work across days.

### Step 1: Understand the user and infer their target

Before building any list, you need the user's positioning. Infer what you can from their role and company; ask only what you cannot infer. Read `references/target-discovery.md` for the full method. In short:
- Establish their **role and company** (ask if not given, or infer from anything they share).
- From that, propose their **ICP and two lanes**: Lane A is the people they sell to or want a relationship with; Lane B is the big creators that their ICP already follows (borrowed reach).
- Ask a few short clarifying questions only for what you could not infer (region, ICP preference, commercial vs brand focus).

### Step 2: Build the focus group list

Research and propose a list of real people worth commenting on, classified into the two lanes, with evidence that each one actually posts. Hand it back to the user to prune. Full method (multi-angle search, hard criteria, classification) is in `references/target-discovery.md`. This works with web search if available, or from names the user provides if not.

### Step 3: Choose who to comment on

With a list in hand, help the user decide who to comment on each time, sustainably. The core idea is a two-tier model (a small core you engage every time, and a larger bank you rotate through with a cooldown so you never feel spammy), plus a daily relevance pick. Read `references/selection-and-cadence.md`.

### Step 4: Generate the comments

You need the actual posts to comment on. In a normal session you cannot pull them from LinkedIn (it blocks that), so ask the user to paste the recent posts of the people you selected, then write one comment per post.

This is the part that makes or breaks everything. A comment that sounds like AI is worse than no comment. Read `references/comment-voice.md` before writing a single comment. The short version: write like a peer, not a professor; one simple idea; in the language of the post; never the over-polished aphorism that screams AI. Always leave the comment ready for the user to read and paste, never auto-post.

If a post links to an article, newsletter, or video, read that content (fetch the link) and comment on something specific from it. Never write "I'll read it" or comment blind on a link you did not open.

## The mindset to carry through all of this

The user is showing up as a peer who adds value, not as an authority correcting people. Every comment should earn its place by being genuine and specific. Volume without quality burns reputation; quality without consistency never compounds. The goal is to become a familiar, valued face to a focused set of people over time.
