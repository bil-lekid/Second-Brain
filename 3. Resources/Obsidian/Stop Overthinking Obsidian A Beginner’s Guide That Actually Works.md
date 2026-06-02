---
tags:
  - Productivity
  - Obsidian
---

![](https://miro.medium.com/v2/resize:fit:875/1*gB_n_LikfBWx3NpaHrrmtA.png)

My Obsidian Graph

As a failed minimalist who migrated 10,000+ notes from Notion to Obsidian, I know exactly what it feels like to overcomplicate things.

After posting my [Obsidian graph time-lapse animation](https://www.reddit.com/r/ObsidianMD/comments/1l4y9jk/i_imported_10405_notion_notes_into_obsidian/) on r/ObsidianMD, somebody asked me for advice on getting started with Obsidian, saying:

> “I’ve watched numerous videos about Obsidian, and I think I’ve overcomplicated things for myself, which has kept me from actually getting started. I’m unsure about how to effectively use tags and folders. Some people suggest avoiding folders altogether to improve linkages between notes and keep the graph clearer. Could you please help me understand the best approach? To give you more context, I want to use Obsidian as a true second brain, a system for note-taking, capturing interesting online information, and linking related notes over time. For example, one note might focus on birds and suitable feeder foods, another on setting up a Raspberry Pi for retro gaming, and others on the books I’ve read, among various topics. Since Obsidian allows linking through tags, I anticipate that these different subjects will eventually intersect and connect.”

This took me back to exactly how I felt when I was first flirting with using Obsidian and spurred me to brain dump all the advice I would have given to myself when starting to use Obsidian.

I was initially lured to Obsidian by the beautiful graph view and the concept of linking notes was a very compelling idea. Not to mention at the time my 10,000+ notes on Notion were becoming very sluggish as all the notes are on the “cloud”, and most importantly I did not want to continue having all my notes held hostage on somebody else’s servers. This duality of pushes from Notion and the alluring pull of Obsidian compelled me to make the leap to Obsidian, but that’s exactly what it felt like, a leap. Not something I could easily or simply do. I had watched countless tutorials and videos of people showing off their crazy vaults and it felt very intimidating. So today I will try to give you the simple & practical steps and guidance to make that transition feel like a gentle step rather than a leap. Whether, like me, you’re coming to Obsidian from Notion, or another app or this is your first time taking notes digitally.

Here’s exactly how to start without getting stuck in setup hell.

## The Counter-Intuitive Mindset Shift

The main thing is to actually start using it and start making notes. Don’t worry about organisation, especially at first. This is a huge mindset shift, but it is necessary.

Most apps and computers in general force you to think about structure and organisation first, then you worry about content. This is flipped with Obsidian, write first, organise never… or at least later.

**Why this works:** Obsidian [search](https://help.obsidian.md/plugins/search) is really good, so you should be able to find what you are looking for purely from search.

**When you do organise:** refrain from folders. Use MOCs and tags instead.

**The folder problem:** A note can only be in one folder, but it may be related to many topics. For example, a note about computational chemistry is related equally to both computer science and chemistry. If you have a Computer Science folder and a Chemistry folder, you either have to:

- Choose one (which isn’t representative of the note)
- Duplicate the note into both folders (now you have two identical notes to manage whenever you want to link or edit)

This entire mess can be avoided by using tags and linking to MOCs.

## How to actually start

### Step 1: Create your Home MOC

When you open Obsidian, create a “Home MOC”. This is just a note named Home MOC. MOC means Maps of Content, but just think of it as a hub to link related notes to and from. Your Home MOC will act as your start point/base. You can link to other important notes and MOCs from your Home MOC for easy access.

You could also set up MOCs for your most important areas/topics like a Finance MOC, Computer Science MOC, etc. and link to them from your Home MOC.

### Step 2: Set up Daily Notes

Enable the [Daily Notes](https://help.obsidian.md/plugins/daily-notes) core plugin. Your Home MOC and daily note will be your two go-to places in Obsidian. I list my tasks/to-do list in my daily note and track daily habits (just using a `- [ ]` checklist) but feel free to do what you want in your daily note. You can think of the daily note kind of like a journal or diary.

Now you have the two main note types that will form the base of your Obsidian journey: Daily Notes and MOCs.

### Step 3: Create essential folders (yes, some folders are okay)

I created a folder for all my daily notes. Why did I create a folder — didn’t I say refrain from folders? Well, you’re right, but Daily Notes are a _type_ of note, not a concept or topic. I know that a daily note will always be a daily note, not a note related to Computer Science or Chemistry. Sure I can link to other notes from/to it, but it will only ever be a daily note. So it’s okay to create folders for _types_ of notes. I only have 6 main folders:

- Daily Notes folder
- MOCs folder
- People folder
- Tasks folder (I like one note per task)
- Notes folder
- [Attachments folder](https://help.obsidian.md/attachments#Change+default+attachment+location)

## Creating your first real note

Let’s walk through a concrete example to see how this all comes together. Say you’ve just read an interesting article about using machine learning to predict chemical reactions.

### Step 1: Create the note

Create a new note with a descriptive title like “ML for Chemical Reaction Prediction — Nature Article 2024”

### Step 2: Add your source

Add the article link at the bottom in a References section:

## References  
- [Original Article](https://example.com/ml-chemistry-article)

### Step 3: Write your content

Write your actual notes — insights, key points, questions, whatever matters to you:

The researchers used a neural network to predict reaction outcomes with 85% accuracy.  
  
Key insight: Traditional quantum chemistry calculations take hours, but this ML model   
gives predictions in seconds.  
  
Question: Could this approach work for drug discovery pipelines?  
  
The training dataset included 50,000 known reactions from organic chemistry literature.

### Step 4: Link to MOCs (the broad connections)

Then I think about [linking](https://help.obsidian.md/link-notes). First, I link to MOCs this note relates to (create new MOCs if needed). For linking to MOCs I now just use tags (in a YAML [property](https://help.obsidian.md/properties), but you could add the tag anywhere in the note like `#ComputerScience`) that are [aliases](https://help.obsidian.md/aliases) for the related MOC. For example in this note I will tag #ComputerScience and #Chemistry:

---  
tags:  
  - ComputerScience  
  - Chemistry  
---

These tags are aliases for their respective MOC. This is better as you get the functionality of tags and the functionality of linking to a MOC note.

**The magic happens automatically.** When you use tags that are aliases for your MOCs, Obsidian treats them as both tags (searchable, filterable) and links (clickable, connected in graph view). Your computational chemistry note now appears connected to both Computer Science and Chemistry topics without being trapped in either folder.

But if that is too much, just directly link to the MOC within the note:

Related MOCs: [[Computer Science MOC]], [[Chemistry MOC]]

### Step 5: Link to specific notes

Finally, link to other relevant notes you’ve already created. You can do this inline, in a property or at the bottom of the note:

This connects to my notes on [[Neural Network Architectures]] and [[Drug Discovery Process]].  
  
See also: [[Quantum Chemistry Limitations]] - this ML approach solves the speed problem I noted there.

**Don’t overthink it.** If this feels like too much structure, just start with the note content and add one or two obvious links. You can always add more links or properties later as your vault grows and patterns emerge.

## Conclusion

This should be enough to get started. But remember, just start writing! This may feel strange as you may feel the compulsion to create some kind of top down organisational structure (whether that be folders or a database) to be able to find the note again or just to feel organised. But if you need to find a note, you can rely on Obsidian’s great search functionality to find what you need when you need it. Prioritise writing over organisation.

### Bonus tip

Avoid trying too many plugins and trying to get that elusive “perfect setup”. The “perfect setup” does not exist, you will always be battling entropy, and no, that new plugin will not suddenly make your vault magically perfect. Avoid the “just one more plugin/tool” trap. I have been down that road and it just wastes time. I went from Trello to multiple Notion database workflows (setting up a mirage of relational databases), to trying Reclaim.ai then to Obsidian with one note per task, then Tasks plugin, and now I am lustfully eyeing the TaskNotes plugin while eagerly awaiting Obsidian [Bases](https://help.obsidian.md/bases) to be released. Even though I can look back and justify each of these transitions for my, _Buzzword warning_, PKM (Personal Knowledge Management) & task management setup, each of these transitions took time away from writing and getting stuff done. I now at least attempt to attain the virtues of being plugin/tool minimalist, despite not fully achieving this ambition. I’m not saying do not use plugins/tools, but just be aware of the real opportunity cost that learning and setting up a new plugin/tool takes. And question if this new plugin/tool or reorganisation is worth the very real opportunity cost. Most of the time, it won’t be.

Remember, the real goal is capturing and connecting ideas, not perfecting your system.

So don’t be a productivity midwit.

Press enter or click to view image in full size

![](https://miro.medium.com/v2/resize:fit:875/1*n5EFs2pqi-IdzOsSLctINA.png)

Just Use Obsidian

Because Obsidian uses local .md files, your notes aren’t trapped in a proprietary system. This safety net means you can finally commit to one tool without vendor lock-in anxiety.

The beauty of this approach is its simplicity. Start with a Home MOC, enable Daily Notes, create a few essential folders, and begin writing. Your vault will grow organically, connections will emerge naturally, and you’ll avoid the endless setup tweaking that keeps many people from actually using their tools.

So commit, don’t be a midwit. 😂