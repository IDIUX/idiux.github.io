# Why and How I Switched from Sketch to Figma — A Story of Design Collaboration
#Blog #Canva/Design

Our entire product design team recently switched from Sketch to Figma as our primary design tool. Sketch is an amazing, mature UI design tool that I’ve loved using for years. It remains superior at drawing vectors and working offline, so it will keep its spot in my Dock for the moment. However, in a team context, Figma has proven to be superior, replacing not just Sketch, but also several other tools.

I’ll talk about why we switched and a whole bunch of things that, as a seasoned Sketch user, I had to [re]learn along the way.

## Seven deadly benefits
* **Simultaneous collaboration.** Once you use this in a team environment, you wonder how you ever did without it.
* **Shared libraries.** Figma allows more fine-grained control of library files and facilitates shared ownership. Cloud hosting allows everyone to get immediate updates. Goodbye Github and Google Drive.
* **Link sharing.** Being able to _super_ quickly share a link to a screen design or a clickable prototype has significantly sped up my cross-discipline team’s workflow. PM approvals and engineering-handovers are a breeze. Goodbye InVision, Sketch Cloud and Zeplin.
* **Version history.** This has replaced messy design folders and file conflicts. Goodbye Github and Google Drive.
* **Licence model.** Our business only has to pay for designers that need to edit the designs — PMs and engineers that only need to view or inspect the files can do so with free accounts.
* **Embedding designs.** We’re still discovering the advantages of embedding Figma designs inside of our Canva docs and presentations. This has opened up new ways for cross-team and cross-discipline communication.

## This new place is exciting and scary
I’ve switched tools so many times in the past, Sketch and Figma look basically the same, how hard could this be? Right? Well, despite their similarities, Sketch and Figma are actually different beasts when it comes to the details.

### What the heck is a frame?
Let’s talk briefly about some fundamental terminology differences. Sketch has _artboards_ whereas Figma has _frames_. Both have _groups_. Figma’s _frames_ are designed to be powerful, flexible and nested, so you use them like you would use both _artboards_ and _groups_ in Sketch. Figma’s _groups_ are less powerful, mostly just used for organising layers.

In Figma, _groups_ automatically change size to accommodate their contents. _Frames_, on the other hand, need to be managed — their dimensions are set when created, either by drawing one from scratch or by converting a _group_ to a _frame_. You can choose whether to show or clip/hide the contents of a frame that extend beyond its bounds (useful for scroll regions). If you change the dimensions of a frame after it’s created, the contents will adjust based on the Constraints you’ve set.

> **Pro tip:** hold down the Command key while using your mouse to adjust the dimensions of a frame without affecting its contents (i.e. ignoring the Constraints).   

_Constraints_ in Figma are the equivalent of _Resizing_ rules in Sketch. They work pretty much the same, although a Figma object’s Constraints will be relative to the _frame_ that contains it (ignoring any _groups_), whereas Sketch’s resizing rules are relative to the parent _group_. Sketch’s rules are easier to configure, but Figma’s are more powerful when combined with Grids (more on that later).

Sketch has _symbols_ contained on their own page, whereas Figma has _master components_ that can be positioned anywhere in the document. There are a few ways you can manage your document’s master components — experiment with what works for you — but the power of being able to make changes to a component in situ and see the effect across all its instances in real-time is amazing. No more switching to the Symbols page, making a change, clicking `Return to instance` and back, over and over…

### How the heck do I select things?
In Sketch, you can hold down the Command key when mouse-clicking to immediately select individual objects, rather than its parent groups or artboard. You can do the same thing in Figma, but it doesn’t work so well because you end up selecting things way too deep, like a vector shape inside an icon, or a text field at the root of an input. A better approach in Figma is to avoid the Command key, hover over the object you want and just keep clicking your mouse. On first click, the top-layer object is selected, usually the frame that contains everything, a double-click will select its child, a triple-click will select its grandchild child, and so on. This differs from Sketch, which requires a double-click (and short pause) to drill down each level. It sounds insignificant, but mastering this click-to-drill-down interaction is key to being productive in Figma — especially as you start holding down Shift to select multiple objects, you start to see how this speeds things up.

In Figma, select and deselect actions are included in the undo stack. This is both good and bad — good for being able to track your (chaotic) changes across many screens on a large canvas, bad for experimentation when you want to undo-redo-undo to compare your changes without having bounding boxes and outlines.

> **Pro tip:** When you select several objects that are visually aligned, some bright pink guidelines appear — the circles allow you to swap objects around and the lines allow you to adjust the padding between all objects at once. It works just like Stacks in Framer X, but you don’t need to do anything in the layer panel to set it up, it just works on the canvas. _So good_.  

### What’s so special about components?
One of the biggest advantages of Figma over Sketch is that you can override many attributes on an instance basis. This includes basic stuff like fill colours and text styles, but you also get access to the visibility of layers _inside_ of instances. An easy example of the benefit of this is for buttons — you can have a single “Primary Button” master component that contains all the different states of that button (normal, active, hover, disabled, loading, etc.), and you can even have different icons or text for each state. Another example is a “Navigation Menu” where you can change which nav item is selected on each different screen while they all remain attached to the master component.

### Where did I put that darn component?
Now that your master components are living right alongside the unwashed masses, rather than in their own gated community, how do you easily find them? Sketch pros are probably using [Sketch Runner](https://sketchrunner.com) to search for symbols. Pressing Control+2 in Figma switches the Layers panel to Components, with the search bar in focus (Control+1 will switch you back to Layers). Once you type your search query, you’re frustratingly unable to select or insert a component using the keyboard, so you’ll have to drag-and-drop the component onto the canvas. [Here’s hoping](https://spectrum.chat/thread/eeafb72b-b558-4ee5-9147-f45585506c65)  they improve keyboard access.

> **Pro tip:** hold down Command+Option while dragging to replace any component instance already on the canvas. In Sketch you achieve this by selecting a symbol instance then using the Symbol select menu in the Inspector panel to drill down through nested folders and long lists of symbols — a much more tedious process.  

### Nesting components like a boss
Organising a system of components in a [shared Library file](https://help.figma.com/collaborating/team-library/team-library) is a great way to get your team working efficiently to produce cohesive designs. As you go crazy creating components, you’ll notice that you can’t nest _master_ components inside each other, but you can nest instances. A popular workflow is to create “building blocks” master components, organised together on a separate page or file, from which you copy instances to construct more complex master components.

A side effect is that these building blocks and various nested components get added to your library and show up in search results in the Components panel. Never fear, in the search results, you can right-click and choose `Remove from library` . Conversely, sometimes you create master components out of a bunch of building blocks, expecting it to be available from other files that use the library, but it’s not there — in the library file, open the Components panel and find/search the component in the list, then right-click and choose `Add to library` .