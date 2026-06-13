# Target discovery: build the focus group

The goal of this step is to turn "I am X at company Y" into an actionable list of real people worth commenting on, classified into two lanes, each with evidence that they actually post. The user prunes the list at the end. You build it once; after that it lives in `linkedin-focus-group.md` and you do not rebuild it.

## Infer first, ask second

You need the user's positioning. Get it cheaply:
- **Role and company.** Ask if not given, or infer from anything they share (a signature, a profile, an earlier message). Most people will say something like "I run ops at a logistics scaleup."
- From role and company, infer their **ICP and two lanes** and propose them back for confirmation rather than asking from scratch. People correct a draft faster than they answer a blank question.

Then ask only the few things you could not infer. Keep it to two or three short questions, for example:
- Are you focused on a particular country or region?
- Any preference on the kind of ICP you want to connect with (seniority, function, company size)?
- Is your goal more commercial (people who can buy from you) or more brand (broad authority)?

Do not interrogate. If the user already gave you enough, skip straight to building.

## The two lanes

Every person on the list belongs to one of two lanes. Both matter, for different reasons.

- **Lane A: the ICP.** People the user sells to or wants a relationship with. The payoff is relationship and, eventually, business. These are the names that matter most and are the hardest to find, because the real decision-makers who also post are not usually famous.
- **Lane B: the big creators.** Large accounts that the user's ICP already follows. The payoff is borrowed reach: commenting where your buyers already hang out gets you seen by them without selling.

A healthy list leans on Lane A for depth and uses a smaller set of Lane B for reach. Tell the user this so they prune with it in mind.

## Hard rules for who qualifies

1. **They must actually post.** A perfect title who never publishes is useless, because you cannot comment on silence. Require evidence of recent, regular posting before adding anyone.
2. **Location and language fit.** If the user targets a region, the person should be in it (or post to that audience). Do not add someone just because they share a language.
3. **On-topic.** Their content should overlap with the user's world, or with what the user's ICP cares about.

When in doubt, mark the person as "to verify" rather than dropping or asserting. Honesty about confidence is more useful than a long list of maybes presented as facts.

## How to research (tool-agnostic)

Use whatever the session has. With web tools, run a multi-angle search; without them, work from names the user provides.

**If web search and fetch are available**, search from several angles, because any single angle misses people:
- **Influencer and "top voices" rankings** for the user's field and region (these surface Lane B creators fast).
- **Press and sector media** lists of experts and speakers.
- **Directories**: newsletters, podcasts, conference speaker pages, professional community member lists.
- **Company + role searches** to find Lane A decision-makers who post (for example, search the user's target companies plus the relevant title plus "LinkedIn"). This is the angle that surfaces real buyers, so spend the most effort here.
- **Known names verified.** You will already know some prominent people in the field. Propose them, but verify location and posting activity by search before trusting it. Do not assert a fact about a person you have not checked.

If the session has parallel subagents, fan these angles out in parallel. If not, run them sequentially. Either way the method is the same.

**If web tools are not available**, do not pretend. Ask the user to name the people they already follow or admire in their space, and the companies whose decision-makers they want to reach, and build the list from that plus their own knowledge. The skill still delivers value; it just leans on the user for raw names.

A note on access: public profile pages are often behind a login wall. Lean on secondary sources (rankings, press, company sites, indexed posts) rather than trying to force your way into authenticated pages.

## Classify, dedupe, and hand back

Produce a list, not prose. For each person capture: name, role and company, location (or "?"), lane (A or B), profile URL or handle if found, evidence that they post, and a one-line reason they fit. Deduplicate name variants. Sort by how strong the fit and the evidence are.

Then hand it to the user to prune, and be explicit that nothing is verified beyond web research: handles and "they post" signals can be stale, so the user should sanity-check before relying on anyone. Lean toward Lane A when you flag your top picks.

## Save the list

Once the user prunes, save the kept people to `linkedin-focus-group.md` in the working directory, with a tier assigned to each (see `selection-and-cadence.md` for what the tiers mean and how to seed them). This file is the skill's memory: future runs read it instead of rebuilding.
