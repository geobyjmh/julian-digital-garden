---
{"dg-publish":true,"permalink":"/digital-garden-using-github-and-vercel/","dg-note-properties":{}}
---


- Link: [[Notes/Personal knowledge management system\|Personal knowledge management system]]
- Link: [[Notes/Digital Garden\|Digital Garden]]

This site works by connecting your Obsidian notes to a publishing system called a digital garden. When you write notes in Obsidian, they stay private unless you explicitly mark them for publishing using a special setting (`dg-publish: true`). Once published, those selected notes are sent to GitHub, which acts as a storage space for your site’s content. From there, Vercel automatically detects changes in the GitHub repository and rebuilds your website so it stays up to date. The result is a live website that displays your chosen notes in a connected, wiki-like format, with features like backlinks, search, and graph views, while everything else in your Obsidian vault remains private and under your control.

# Tutorial
**Phase 1: The "Engine" (GitHub & Vercel)**

We need a place for your notes to live online. We'll use a template that does all the coding for you.

1. **GitHub:** Go to [GitHub](https://github.com/oleeskild/obsidian-digital-garden) and click **"Use this template"** > **"Create a new repository."**

- Name it something like my-garden.
- Set it to **Public**.

3. **Vercel (The Host):** Go to [Vercel](https://vercel.com/) and sign up with your GitHub account.

- Click **"Add New"** > **"Project."**
- Import the my-garden repository you just made.
- Click **Deploy**.
- _Result:_ You now have a live URL (e.g., my-garden.vercel.app), but it's currently empty.

---

**Phase 2: The "Bridge" (Obsidian Setup)**

Now we tell Obsidian how to talk to GitHub.

1. **Install the Plugin:** In Obsidian, go to **Settings** > **Community Plugins** > **Browse**. Search for **"Digital Garden"** and install/enable it.
2. **Create a GitHub Token:**

- Go to your GitHub [Developer Settings](https://github.com/settings/tokens).
- Generate a "Fine-grained token."
- Give it **Read/Write** access to "Contents" for your my-garden repo.
- **Copy this token immediately!**

4. **Configure Plugin:** In Obsidian, go to the Digital Garden plugin settings:

- **GitHub Username:** Your username.
- **GitHub Repo:** my-garden.
- **GitHub Token:** Paste the token you just copied.
- **Base URL:** Your Vercel link (e.g., [https://my-garden.vercel.app](https://my-garden.vercel.app)).

---

**Phase 3: Tending the Garden (Publishing)**

Your garden is ready. Now you just need to pick which notes to "plant."

**1. Mark a note for publishing**

The plugin only publishes notes that have specific "frontmatter" (data at the very top). At the top of your note, type this exactly:

Markdown

---

dg-publish: true

---

**2. Set your Homepage**

One note needs to be your "Home." Add this to that specific note:

Markdown

---

dg-publish: true

dg-home: true

---

**3. Hit the Publish Button**

- Look for the **Garden icon** on your left sidebar (or press Cmd/Ctrl + P and type "Digital Garden: Publication Center").
- You will see a list of changed notes. Click **Publish**.
- Wait about 60 seconds, and your site will update!

---

**Pro-Tips for your Experiment**

- **Links:** Use [[Note Name\|Note Name]] as usual. The plugin automatically turns these into web links.
- **The "Hard Work" is gone:** You never have to touch Wix or code again. You just write a note, add dg-publish: true, and click one button.
- **Private vs Public:** Only notes with that dg-publish tag will ever leave your computer. Everything else stays private.

Does that feel more manageable than the Wix setup you were trying before?