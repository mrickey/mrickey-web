---
id: 2747
title: 'From LogSeq to Gemini'
date: '2025-05-29T16:22:16-07:00'
author: af6fb
excerpt: "I have been working through some things in my mix of software lately. The key area I've been struggling with is my note taking tools. I'm currently using LogSeq, but I've used Notion, Obsidian, Evernote, and Keep. There are many others I haven't looked at yet."
layout: post
guid: 'https://mrickey.com/?p=2747'
permalink: /2025/05/29/from-logseq-to-gemini/
activitypub_status:
    - federated
image: '/wp-content/uploads/2025/05/2025-05-29-Gemini-88x88.png?crop=1'
categories:
    - Technology
format: false
---

This morning I watched a video about NotebookLM and its ability to ingest multiple pieces of content and build a knowledgebase without any outside influences. Basically, your documents are the only things it uses to build "your" knowledge system.

I started thinking about LogSeq and what it does for me. I like how I can create documents on the fly and easily jump between them. At the bottom of each page is a list of all inbound links so I can see connections. Search is good, and the UI is easy to work with. LogSeq supports a wide variety of platforms and is open source.

As much as I like LogSeq it has some shortcomings. I cannot self-host a sync server (for sharing across devices), it does not support collaboration (multiple people working in the system), and it oddly does not support printing. Actually, neither do Notion or Obsidian. The LogSeq team is talking about adding these capabilities, but I'm not sure I want to wait.

I decided to explore this idea of using Google as my PKM. So I did what any modern thought explorer would do...I ask Gemini.

Here is my prompt and the response. Interestingly, I didn't feel a need to ask more questions.

## The prompt

I want to talk about an idea I have. I am currently using LogSeq to keep track of my notes and reference material. In the past I have used apps like Notion and Obsidian. These have worked well for me. But, with the benefits of Google AI and NotebookLM I'm wondering if I could get most of this functionality using Google Docs, Sheets, Slides, and PDF files to get the same capability.

How would you compare Google's Gemini and NotebookLM to the features and capabilities of the apps I mentioned?

## The Response

That's a fantastic idea to explore! Leveraging Google's AI capabilities with familiar tools like Docs, Sheets, and Slides, combined with NotebookLM, could indeed create a powerful personal knowledge management (PKM) system. Let's break down how it compares to LogSeq, Notion, and Obsidian.

### Understanding Your Current Tools

- **LogSeq:** A privacy-first, open-source knowledge base focusing on daily journaling, bidirectional linking (like a "Zettelkasten" system), block references, queries, and a graph view. It's strong for interconnected notes, task management, and PDF annotations.
- **Notion:** An all-in-one workspace that combines note-taking, project management, databases, wikis, and more. It's highly customizable, offering flexible page structures, linked databases, and collaboration features. Notion is excellent for structured organization and team collaboration.
- **Obsidian:** A markdown-based note-taking app that emphasizes local-first storage, bidirectional linking, and a powerful graph view. It's known for its extensive plugin ecosystem, allowing for deep customization and functionality tailored to individual needs. Obsidian offers a high degree of control over your data.

### Google's Ecosystem: Docs, Sheets, Slides, PDFs, Gemini, and NotebookLM

**Google Docs, Sheets, and Slides (Core Functionality):**

- **Collaboration:** Real-time co-editing, comments, suggestions, and version history. This is a strong point for shared knowledge.
- **Accessibility:** Cloud-based, accessible from any device, and supports offline editing.
- **Basic Organization:** Folders in Google Drive, document outlines, and search.
- **Integration:** Seamlessly integrates with other Google Workspace apps (Gmail, Calendar).
- **PDF Viewer:** Built-in PDF viewing in Chrome, with extensions (like Adobe Acrobat) offering annotation, highlighting, and conversion.

**Google Gemini (AI Assistant):**

- **Content Generation:** Can assist with drafting text, summarizing, and generating ideas within Docs, Sheets, and Slides (e.g., "Help me refine" in Docs, "Help me analyze" in Sheets).
- **Information Retrieval:** Can answer questions and provide information based on broad knowledge or even within the context of your open Chrome tab.
- **Summarization:** Quickly condense information from various sources.
- **Task Automation (Workspace Flows):** Can automate multi-step processes using custom AI agents (Gems) to research, analyze, and generate content, referencing your Drive files for context.

**NotebookLM (Your AI Research Assistant):**

- **Source-Grounded AI:** This is a key differentiator. NotebookLM allows you to upload a wide variety of sources (Docs, PDFs, web URLs, YouTube videos, audio files) and then chat with an AI that's "grounded" in *your specific content*. It provides citations back to your sources, building trust and allowing you to verify information.
- **Summarization &amp; Synthesis:** Generates summaries, extracts key information, and makes connections between different sources.
- **Interactive Learning:** You can ask direct questions, refine responses, and even get "Audio Overviews" that turn your sources into podcast-style summaries with interactive modes.
- **Idea Generation:** Can help brainstorm, suggest angles, or create outlines based on your uploaded material.
- **Study Guides:** Can generate structured study guides from your documents.
- **Privacy:** Google states that your personal data (uploads, queries, responses) is *not* used to train NotebookLM's models.

### Comparison: Can Google's Ecosystem Replicate Your PKM?

Let's break it down by feature:

**1. Bidirectional Linking &amp; Graph View:**

- **LogSeq/Obsidian (Strong):** This is where they excel. Their core design is built around linking notes and visualizing those connections in a graph. This helps discover relationships and build a "web of knowledge."
- **Notion (Moderate):** You can link pages within Notion databases, creating relationships, but it lacks a visual graph view like LogSeq or Obsidian.
- **Google Ecosystem (Weak for direct linking, strong for AI connections):**
    - **Direct Linking:** Google Docs has internal linking (bookmarks, table of contents), and you can link between Docs/Sheets/Slides using URLs. However, it's not the same as the "block-level" or "page-level" bidirectional linking seen in LogSeq/Obsidian where links are automatically created or easily surfaced.
    - **AI-Powered Connections:** This is where Gemini and NotebookLM come in. While they don't offer a visual graph, they can *analytically* connect ideas across your documents. NotebookLM, in particular, can identify relationships and synthesize information from disparate sources, effectively creating a "semantic graph" behind the scenes that you interact with through conversation. This is a different paradigm but can achieve a similar goal of surfacing related information.

**2. Daily Notes &amp; Journaling:**

- **LogSeq (Excellent):** Designed for daily notes with automatic date-based pages, making it ideal for journaling and capturing fleeting thoughts.
- **Notion/Obsidian (Good):** Can be set up for daily notes, but it's not as natively integrated as in LogSeq.
- **Google Ecosystem (Moderate):**
    - **Google Docs:** Can be used for daily journaling, but it requires manual creation of new documents or a template.
    - **Google Calendar/Keep:** Can be used for quick notes and reminders, but not for long-form journaling or interconnected daily entries.
    - **Gemini/NotebookLM:** Can assist with summarizing your journal entries or extracting themes if you feed them in, but they don't provide the daily note *structure*.

**3. Task Management:**

- **Notion (Excellent):** Powerful databases with Kanban boards, calendars, and customizable workflows make it a strong project and task manager.
- **LogSeq/Obsidian (Good):** Both offer robust task management features with queries to aggregate tasks.
- **Google Ecosystem (Moderate to Good):**
    - **Google Tasks/Keep:** Basic task management.
    - **Google Sheets:** Can be used for more complex task tracking with formulas and conditional formatting.
    - **Google Docs (Smart Chips):** Can integrate tasks and checklists directly into documents.
    - **Gemini/Workspace Flows:** The potential here is significant. Workspace Flows could automate task creation, assignment, and tracking based on document content (e.g., extracting action items from meeting notes).

**4. PDF Annotation &amp; Management:**

- **LogSeq (Good):** Directly supports PDF highlighting and annotation.
- **Obsidian (Via Plugins):** Can extend functionality to include PDF annotation.
- **Notion (Embed/View):** Can embed PDFs but typically doesn't offer robust direct annotation.
- **Google Ecosystem (Improving):**
    - **Chrome PDF Viewer:** Basic viewing.
    - **Adobe Acrobat Extension:** Offers more advanced annotation and editing features within Chrome.
    - **NotebookLM:** Crucially, NotebookLM can *ingest* PDFs (and even scanned documents) and allow you to ask questions about their content, summarize them, and extract information. This is a powerful form of "annotation" through AI.

**5. Querying &amp; Information Retrieval:**

- **LogSeq/Obsidian (Excellent):** Powerful query languages allow you to pull specific information across your entire knowledge base.
- **Notion (Excellent):** Database filters and views provide strong querying capabilities.
- **Google Ecosystem (Strong with AI):**
    - **Google Drive Search:** Powerful keyword search across all your documents.
    - **Gemini:** Can answer questions and summarize information you ask it.
    - **NotebookLM:** This is the game-changer here. You can ask NotebookLM sophisticated questions about your uploaded documents, and it will provide answers grounded in your sources, effectively acting as a highly intelligent query engine for your personal knowledge base.

**6. Customization &amp; Extensibility:**

- **Notion (Excellent):** Highly customizable page layouts, databases, and templates.
- **Obsidian (Excellent):** Massive plugin ecosystem allows for virtually limitless customization and integration.
- **LogSeq (Good):** Supports plugins and themes for customization.
- **Google Ecosystem (Growing with AI):**
    - **Docs, Sheets, Slides:** Offers templates, add-ons, and some customization.
    - **Gemini/Workspace Flows:** The ability to build custom AI agents (Gems) and automated workflows offers a new level of "extensibility" that goes beyond traditional software plugins. You're customizing how AI interacts with and processes your information.

**7. Data Ownership &amp; Portability:**

- **LogSeq/Obsidian (Excellent):** Your data is stored locally as Markdown files, giving you full ownership and easy portability.
- **Notion (Cloud-based):** Data is in the cloud. Export options are available but less direct than local files.
- **Google Ecosystem (Cloud-based):** Your data is stored in Google Drive. While you own your data and can export it, it's not in a simple, universally portable format like plain Markdown files for easy migration to another tool. However, the ubiquity of Google Workspace makes sharing and collaboration very easy.

### Your Idea: A Viable Approach?

Yes, your idea is absolutely viable and could be very powerful, especially with the advancements in Gemini and NotebookLM. Here's why and how it might work:

**Strengths of the Google Ecosystem for PKM:**

- **Centralized AI Powerhouse:** Gemini and NotebookLM are the core advantages. They can understand, summarize, connect, and even generate new content based on your existing notes and reference materials. This moves beyond simple search to intelligent insight generation.
- **Existing Document Infrastructure:** You're already familiar with Docs, Sheets, and Slides. These provide robust tools for creating and organizing different *types* of information (documents, structured data, presentations).
- **Familiarity &amp; Collaboration:** The collaborative features of Google Workspace are industry-leading, making it easy to share and work on notes with others if needed.
- **Accessibility:** Your knowledge base is available anywhere, on any device.
- **PDF Integration:** NotebookLM's ability to "read" and interact with your PDFs is a significant benefit for research.

**How You Might Implement It:**

- **Google Docs for Notes:** Use Docs for your individual notes, daily entries, meeting notes, etc. Leverage "smart chips" for linking, and document outlines for structure.
- **Google Sheets for Databases/Trackers:** If you have structured information (e.g., project tasks, reading lists, contact lists), Sheets can act as your "database" similar to Notion's databases.
- **Google Drive for Organization:** Use a well-structured folder system in Google Drive to organize your Docs, Sheets, Slides, and PDFs.
- **NotebookLM as your "Brain":**
    - **Upload Everything:** Feed all your important Docs, Sheets, PDFs, even relevant web pages or YouTube videos into NotebookLM. Create different notebooks for different topics or projects.
    - **Ask Questions:** Instead of just searching, ask NotebookLM direct questions about your notes. "What are the key takeaways from my research on X?" "Summarize the arguments for Y in these three articles." "What tasks did I identify for Project Z?"
    - **Synthesize Ideas:** Use NotebookLM to help you connect seemingly disparate ideas from different sources. "What are the connections between this meeting note and that research paper?"
    - **Generate Content:** Ask it to draft outlines, summaries, or even initial drafts of reports based on the information it has access to.
    - **Audio Overviews:** For long documents or complex topics, use the audio overview feature to "listen" to your research.
- **Gemini (Browser/Workspace) for Quick Access &amp; Broader Context:**
    - Use Gemini in Chrome to quickly summarize web pages you're referencing.
    - Leverage Gemini directly in Docs or Sheets for writing assistance or data analysis on the fly.

**Potential Downsides/Considerations:**

- **Lack of Native Graph View:** If the visual "web of knowledge" is crucial for your thinking process, you won't get that directly. However, the AI's ability to *surface connections* might suffice or even be superior for complex information.
- **No Markdown-First Editing (for native files):** Google Docs is not a Markdown editor. If you're deeply ingrained in Markdown, this might be a small adjustment. However, Docs can *import* Markdown, and NotebookLM can ingest plain text.
- **Less "App-Centric" Feel:** It's more of a modular system using multiple Google tools rather than a single, all-encompassing app like Notion. This can be a pro or con depending on your preference.
- **Offline Access (Nuance):** While Google Docs supports offline editing, the AI capabilities of Gemini and NotebookLM generally require an internet connection.

**Conclusion:**

Your idea of using Google Docs, Sheets, Slides, PDFs with Gemini and NotebookLM is not just feasible, it's a very forward-thinking approach to PKM. While you might miss the *visual graph view* of LogSeq/Obsidian, the *analytical and generative capabilities* of Gemini and NotebookLM could provide a far more powerful way to interact with your knowledge. NotebookLM, in particular, acts like an AI assistant specifically trained on *your* information, allowing for deeper insights and more intelligent information retrieval than traditional search or linking alone.<sup></sup>

It's definitely worth experimenting with. Start by feeding a collection of your existing notes and reference materials into NotebookLM and see how it transforms your ability to understand and leverage that information. You might find it offers a new, more intuitive way to manage your knowledge.

There was also a long list of sources it referenced, but I couldn't find a way to copy it for inclusion here.

The response to my short prompt was incredibly thorough and I found it to be very accurate based on my experience with the different apps.

As an experiment, I spent a about fours hours working to put a small branch of my graph (or knowledge base) into Google Docs to see if I could make this work. In general it felt OK...at first. In the next sections I will talk about my results.

## Using LogSeq

What do I like about LogSeq? LogSeq is fast and easy to navigate, partially do to its searching capabilities. Entering text is fast, since I became comfortable with [markdown](https://www.markdownguide.org/cheat-sheet/). Links are the real performance increase however. I can simply type a page name inside a double pair of square brackets. As I start to type the page name I get a filtered list of matching pages and the ability to create a new page. I simply can't explain how quick and easy this is. Beyond creating the link, each page has back links. This is a list of all pages linking to the document. This makes navigating between related pages really easy.

On the downside, LogSeq does not allow me to collaborate with others. This means my wife and I work on documents together. It also doesn't offer the ability to print a page. There is a way to export to PDF, but there is a lot of formatting that doesn't make the journey.

## Using Docs

Docs (or sheets, slides, etc) offer a great editing experience. Although I find I have to do more through hotkeys and menus. I like sharing documents and folders with my wife, this allows us to access and update information to make sure it is current.

Docs does a better job of recognizing spelling and grammar errors, something I appreciate. It also makes nicer looking documents. It can show a document outline on the left, and that feels good to my brain. Basically, I like creating documents in Docs.

For my needs, Docs does a lot of what I need. It has sharing and collaboration well under control. I can access it from a variety of platforms. This is why Docs has been my primary office tool for years, and I don't see that changing any time soon. Oh, and I can print documents.

What I quickly discovered was how difficult it is to link documents in Docs. I have to press CTRL-K, enter the text for the link, then the URL for the link. Docs does help with this, as it will narrow down a list of files and folders in Drive as the target for a link. Yes, I said Folders. In Docs I can insert a link to a folder, pressing the link will open Drive and show the selected folder. Nice.

But, Docs requires me to create the link target first and this really messes with the flow I've become so comfortable with. It also made me much more thoughtful about my folder structure...something I don't think about at all with LogSeq or Obsidian. Notion is different as it supports the concept of folders for organizing notes.

## Using NotebookLM

NotebookLM is wonderful. If you haven't tried it, you should at least look at a video or two.

NotebookLM uses the documents you associate with it and creates a knowledgebase based on those document. It does not collect related information from any other source. This helps prevent hallucinations and other AI artifacts. It does not share your document content or use it to train the larger AI engine.

 NotebookLM is not without its own issues. First, and this is probably the biggest, I can only include 50 files. This may be because I don't have one of Google's paid AI subscriptions or because I'm using it outside of a Workspace account. This leads to the second problem...I have to add each file individually. I would much prefer to give NotebookLM a Google Drive folder and let it ingest all of the files in that folder. It should look for document changes, additions, and deletions. In addition to Google Docs files it should pick up images, PDFs, and any other files that might be there.

## Conclusion

While this has been a fun experiment, I don't think Google is ready to take over my knowledge graph and help to maintain my notes. I do think Google isn't too far away at this point. If they could remove some friction and create an app that makes traversing notes easier I would definitely give it a try.

What are your thoughts on note taking apps...what do you like? What features are you having trouble finding?