---
name: jetpost-share-for-feedback
description: Suggest who to share a Jetpost note with for feedback, then share it. Use once the user has written a Jetpost note and the draft looks finished, or when they ask who they should send a note or an idea to.
---

# Share a note for feedback

Goal: suggest a few people this user should send *this* note to, then share it with the ones they pick.

## 1. Suggest people

Read the note first (Jetpost's `get_note` tool if you don't have it). Then suggest 3–5 people, each with one line on why. Use what you already know about the user and who they work with, and the people they already share Jetpost notes with (`list_members`).

Good picks work on or care about the note's topic, would be affected by it, or are people the user already goes to for opinions.

If you don't know enough to suggest anyone, ask the user who they had in mind.

## 2. Share

Ask which ones to send it to. Don't share anything until the user picks.

Add the people they picked with `share_note`. Turn on `notify` only if the user wants Jetpost to email them. Otherwise, give the user the note's link so they can send it themselves.
