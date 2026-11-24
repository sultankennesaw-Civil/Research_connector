# Research Connector

A bubble-style inventory for research papers, so you never forget **why** you saved a paper.

```
Virtual Reality (VR)
 └─ What improves learning in VR
     └─ Interaction (e.g. pressing the trigger)
         └─ 📄 Paper  💡 "Pressing the trigger → people interacted and learned more"
```

Each topic is a bubble. Click a bubble to go inside it. Papers sit inside the topic they support. Each one keeps a
**"💡 Why I saved it"** note, so later you can see what you were looking for in that paper.

## How to use it

1. Download or clone this repository to your PC.
2. Put your PDFs in the `papers/` folder.
3. Double-click `index.html` (Chrome or Edge recommended).
4. Click **Data ▾ → Save to a data file…** and save `research-data.json` in this folder.
   From then on, every change is saved to that file automatically.

### Folder layout

```
Research_connector/
├── index.html          ← the app (open this)
├── research-data.json  ← your topics, papers and notes (created by the app)
└── papers/             ← your PDFs
    └── some-paper.pdf
```

## Features

- **Nested bubbles**: Topic → sub-topic / finding → … → papers, as deep as you like.
- **Why-I-saved-it notes** on every paper, stored separately for each topic. The same paper can sit under several
  topics, with a different note for each.
- **Open PDF** straight from the paper card. Use **Choose PDF from papers folder…** to link a file.
  Full paths such as `C:\Users\me\Papers\x.pdf` also work.
- **Search** (press `/`) across topic names, notes, paper titles, authors, tags and your why-notes.
- **All papers** library view, with the topics each paper is filed under.
- Edit: click the centre bubble, or right-click any topic bubble. Move topics with **Move under**.
- Go back with the breadcrumb at the top, by pressing `Esc`, or by double-clicking the centre bubble.
- **Backups**: Data ▾ → Export / Import `.json`. These work in every browser.

## Saving: where your data lives

| Browser | How it saves |
|---|---|
| Chrome / Edge | Directly into `research-data.json` after you pick it once. The app asks you to "Reconnect" it when you reopen. |
| Firefox / Safari | In the browser's own storage. Use **Export backup** regularly and **Import** on another PC. |

## Privacy note

This repository is **public**. `.gitignore` keeps your PDFs (`papers/*.pdf`) out of git by default, because
published papers are usually copyrighted. If your notes are private, also keep `research-data.json` out of git
(uncomment the line in `.gitignore`).
