---
name: jetpost-share-for-feedback
description: Suggest who to share a Jetpost post with for feedback, then help send it. Use once the user has written a Jetpost note (after create_note, when the draft looks finished), or when they ask who to send an idea to, who to get feedback from, or who they work with most.
---

# Share a post for feedback

Goal: a short list of 3–5 people this user would actually ask for feedback on *this* idea, then help them send it.

## 1. Work out who they talk to

Use whatever is available, in this order, and stop once you have about 15 candidates:

- **Prior chats and memory**: people the user has mentioned, especially as collaborators, their manager, or people whose opinion they cite.
- **Slack**: who they DM and group-DM with most in the last ~60 days.
- **Calendar**: recurring 1:1s and small meetings (5 people or fewer) in the last ~60 days.
- **Gmail or Outlook**: who they've emailed directly in the last ~60 days. Skip newsletters, notifications and large lists.

Use these sources only to identify people and how often and how recently the user talks to them. Don't quote or summarize anyone's messages back to the user.

If no connectors are available, say so plainly and suggest connecting Slack, or Gmail and Calendar, in the app's connector settings, since that makes these suggestions much better. Meanwhile, suggest people from prior chats and ask the user who else comes to mind.

## 2. Rank for this idea

Read the post (Jetpost's `get_note` tool if you don't have it). From the candidates, prefer people who:

- work on or care about the post's topic, or would be affected by it
- the user already trusts for opinions (frequent 1:1s, cited in past chats)
- will actually reply (recent contact beats old contact)

Include one unexpected but useful pick if there's a good one, such as someone on an adjacent team.

## 3. Present

Two short groups, each person with one line on why:

- **Closest collaborators**: the people they talk to most
- **Most relevant to this idea**

Ask which ones to send it to. Don't send anything until the user picks.

## 4. Send

New notes are private, so add the people they picked as recipients first, so they can read it: call `list_members`, then `share_note` with their ids. Leave `notify` off, since your message is how they'll hear about it.

For each person they choose, draft a short, personal message in the user's voice, with the post link and a specific ask ("would love your take on the pricing section"). Use the channel they use most with that person: a Slack DM, or an email draft.

Show the drafts and send only after the user approves them. If no messaging connector is available, give the user the link and the drafts to paste.
