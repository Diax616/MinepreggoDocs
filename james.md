# Figura vs. CPM: A Blockbench Artist's Guide to Custom Player Models

Hey there! So you're making awesome custom models in Blockbench and you want to get them into Minecraft. You've probably heard of **Figura** and **Customizable Player Models (CPM)**, and you're wondering which one to use. 

Since you're an artist and not a coder, I'm going to skip all the nerdy Java, Forge, and vanilla Minecraft engine talk. We're just going to focus on what matters to you: **how your art gets into the game, how it behaves, and how much of a headache the setup will be.**

Here is the breakdown of Figura vs. CPM, tailored specifically for a 3D artist.

---

## The Quick Vibe Check

*   **Figura:** The current crowd favorite. It treats your model as a completely separate "Avatar." It's highly modular, has a massive community, and uses a real-world coding language (Lua) that has a million tutorials online.
*   **CPM (Customizable Player Models):** The older, slightly more niche sibling. It treats your model more like a "heavy modification" of the base player. It uses its own custom-made coding language, which means fewer tutorials and a steeper learning curve if you want to add cool interactive effects.

---

## 1. Overwriting the Base Model (The "Look")

As an artist, your biggest question is probably: *"How do I get rid of vanilla Steve/Alex, and how do I put my custom mesh in their place?"*

### Figura: The "Full Costume" Approach
Figura doesn't just tweak the vanilla model; it completely replaces it with an **Avatar**. 
*   **Total Control:** You can hide every single piece of the vanilla Steve model (head, body, arms, legs, jacket, etc.) with a single click in the Blockbench plugin. 
*   **Custom Rigs:** You aren't forced to use the vanilla bone structure. You can build a completely custom rig in Blockbench (like a quadruped, a robot with different joint placements, or a floating ghost), and Figura will render it exactly as you designed it.
*   **Swapping:** Because it's an "Avatar," you can have multiple completely different models saved and swap between them in-game instantly without restarting.

### CPM: The "Bolt-on" Approach
CPM is built around the idea of customizing the *existing* player model.
*   **Vanilla Tied:** While you *can* hide the vanilla model and replace it, CPM's engine is deeply tied to the vanilla player rig. It works best when you are keeping the basic humanoid shape and just adding cool armor, wings, tails, or changing the textures.
*   **Custom Rigs:** You can do custom rigs, but it can sometimes feel a bit more restrictive or "janky" compared to Figura when you try to break completely away from the standard human skeleton.

**Artist Verdict:** If you want to make a completely non-humanoid character (like a dragon or a mech), **Figura** is going to give you a much smoother time. If you just want to make a really cool anime character or custom armor set that still walks like a human, **both** will work fine, but CPM is historically built for this.

---

## 2. Accessing Data from Other Mods (The "Crossover")

Let's say you're playing with a magic mod that adds a "Mana" bar, or a tech mod that adds a jetpack. You want your custom model to react to these mods (e.g., your model's eyes glow when mana is low, or your custom wings flap when the jetpack is on). 

*How do your models talk to other mods without you needing to learn Java?*

### Figura: The Universal Translator
Figura has a built-in "bridge" (called an API, but think of it as a translator) that allows it to read data from almost any other mod.
*   **Plug-and-Play:** Figura can automatically read the health, armor, held items, and status effects of the vanilla game. 
*   **Mod Support:** Because Figura is so popular, many mod developers actively write "hooks" for it. This means if a mod adds a new mechanic, they often include built-in support so Figura avatars can react to it.
*   **How you use it:** You just write a tiny bit of simple code (in Lua) that says, *"Hey game, what's my mana level?"* and then you tell your Blockbench model to change colors based on that number. 

### CPM: A Bit More Closed Off
CPM is great at reading vanilla Minecraft data (health, weather, time of day), but it struggles a bit more with third-party mods.
*   **Manual Setup:** To get CPM to read data from a specific third-party mod, the creator of that *other mod* usually has to specifically add CPM support to their code. 
*   **Less Cross-Mod Magic:** If the mod author didn't specifically code CPM support, your model won't be able to read that mod's data. It's a bit more isolated from the wider modding ecosystem compared to Figura.

**Artist Verdict:** If you want your models to react dynamically to a heavily modded game (like RLCraft or massive modpacks), **Figura** is the clear winner. It just "gets" other mods much better out of the box.

---

## 3. The Scripting Headache (Making Things Move)

You've exported your model, but now you want the tail to wag when you walk, or the wings to fold when you sneak. You need to use the mod's scripting language.

*   **Figura uses Lua:** Lua is a real, industry-standard programming language. If you get stuck, you can go to YouTube, Reddit, or the Figura Discord, and there are **thousands** of tutorials, copy-paste code snippets, and people willing to help you. 
*   **CPM uses "CPM Script":** This is a custom language made specifically for CPM. It looks a bit like Java/C++. The problem? Because it's custom, **there are very few tutorials online**. If you get stuck, you're mostly relying on digging through the official wiki or asking in their Discord. 

**Artist Verdict:** Unless you already know how to code, **Figura** will save you hours of frustration simply because the community resources and tutorials are vastly superior.

---

## 4. The Blockbench Workflow

Both mods have official plugins for Blockbench to help you export your models, textures, and animations.

*   **Figura's Plugin:** Very polished, frequently updated, and integrates beautifully with Blockbench's animation timeline. Exporting an "Avatar" folder with all your scripts, models, and textures takes just a few clicks.
*   **CPM's Plugin:** Also works well and gets the job done, but Figura's plugin generally feels a bit more user-friendly for beginners and has a more active development cycle.

---

## 5. Community and Resources

*   **Figura:** Massive Discord server, tons of public avatars you can download and study, active YouTube tutorials, and a super detailed wiki. If you need help, you'll find it fast.
*   **CPM:** Smaller community, fewer public resources, but still has dedicated users and some cool examples. Just expect to do more digging on your own.

---

## The Final Recommendation

**Go with Figura if:**
*   You want to make completely custom, non-humanoid rigs.
*   You want your models to easily react to items and mechanics from other mods.
*   You want access to a massive community, tons of tutorials, and easy-to-find code snippets for your animations.
*   You want to swap between totally different character models on the fly.

**Go with CPM if:**
*   You are strictly making humanoid characters (keeping the basic Steve/Alex skeleton).
*   You are playing on an older version of Minecraft where CPM might have better legacy support (though Figura is catching up/has caught up in most versions).
*   You specifically prefer CPM's rendering engine or shader effects (CPM has some really cool built-in visual effects, though Figura has them too now).

---

## TL;DR for the Artist

**Figura** is currently the gold standard. It's more flexible for custom rigs, plays much nicer with other mods, and has a massive community to help you when your tail animation breaks. Download the Figura Blockbench plugin, grab a free avatar from their Discord to look at how it's built, and start tweaking! Happy modeling!