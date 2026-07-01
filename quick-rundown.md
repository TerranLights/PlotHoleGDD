# Quick Rundown

## Design Pillar: The Illusion of Agency

This is a visual novel wearing an RPG's skinsuit. Every system that *looks* like a meaningful choice — character creation, dialogue — is cosmetic and produces identical outcomes no matter what you pick. The only things in the game with real mechanical effect are the tray-carrying mechanic and upgrades earned during play (see Upgradable Robot Body). Everything else is flavor text dressed up as a decision, and the game never bothers hiding that from the player — it's the joke, not a secret.

## Character Creation

it'll be **C.L.A.N.K.E.R.**:
- **C**ore // (akin to Strength and Constitution) — carrying capacity, how many trays/items you can haul, how much impact damage you shrug off
- **L**ucidity // (akin to Perception) — spotting hidden compartments, glitches, and the passenger who's clearly lying about what they ordered
- **A**gility // (exactly like in Fallout) — move speed, balancing trays while running, not spilling drinks on the guy in the dining car
- **N**erve // (probably) — resistance to jump-scares, glitch-outs, and passengers screaming about their missing luggage
- **K**now-How // (akin to Intelligence) — hacking terminals, repairing broken train cars, deciphering garbled quest logs
- **E**mpathy // (akin to Charisma and/or Humanity) — talking passengers down, better tips, unlocking the "actually helpful" dialogue options
- **R**esilience // (akin to Endurance) — how much wear-and-tear your chassis takes before you need a tune-up

Stats are chosen at chassis assembly (character creation) — and, per the Design Pillar above, **they don't actually do anything.** Every build plays identically; the descriptions above are flavor text for your character sheet, not real modifiers. This mirrors the Non-Dialogue System: the RPG trappings are cosmetic, and the joke is that the game never bothers to hide it.

## Non-Dialogue System

Most conversations don't actually offer real choices — that's the joke. Regardless of which option you pick, the passenger mostly hears what they want to hear (or the game glitches past your input entirely):

- Yes
- No but Yes
- Sure, haha
- What?

**How it actually works under the hood:**
- The options are flavor, not branches — the underlying quest state advances the same way no matter what you pick.
- Occasionally (weighted by **Empathy** or **Nerve**) the game *pretends* to notice which one you picked and throws in a one-off reactive line, then continues exactly as before. This is the bit — players slowly realize their choices never mattered, and the game leans into that instead of hiding it.
- Rare "true" branches exist but are disguised as more of the same four options, so players can't tell which conversations are the real ones without paying attention (rewards high-**Lucidity** builds).
- Some NPCs are aware the dialogue is fake and comment on it directly (fourth-wall passengers).

## World & Passengers

You're a service droid working for **Pagliarulo Railways**, aboard a train that is, gameplay-wise, physically and literally on rails — the whole game is one long corridor with detours, and the premise makes that a joke instead of a limitation.

The train is endless, procedurally re-shuffling its cars between visits, so no two trips through "the same" car look identical (a soft justification for reused assets and a Bethesda-style long loading corridor gag).

**Sample passengers:**
- **The Spy** — insists every fetch quest is actually a covert op ("bring me a glass of water" becomes a dead-drop). Never breaks character even when the "water" is just water.
- **The Retired Space Pirate** — wants his stuff *exactly* how it was on his old ship, gets irrationally upset over minor substitutions, secretly just lonely.
- **The Sentient Suitcase** — a passenger in its own right, files its own fetch quests, low-key trying to escape the train.
- **That One Guy in the Dining Car** — always there, no matter which car you think you're in. Never acknowledged as strange by other NPCs.

Quest types: literal fetch (comically over-engineered), radiant/repeatable filler requests, and "broken" quests where the objective glitches mid-delivery and you have to improvise.

## Core Gameplay Loop

**One mechanic:** carry a tray, keep it balanced, don't spill, don't run out of time. Everything else is dressing on top of that single verb — no combat, no branching skill trees, no route-planning. Just get better at carrying trays through chaos.

1. **Receive order** — a request is generated from three shuffled pools (see Quest Generation below).
2. **Traverse** — carry the tray through shifting, glitchy cars while your battery drains (see Power Meter); balancing/timer pressure is the actual challenge.
3. **Deliver** — non-dialogue exchange resolves the quest regardless of what you "said."
4. **Update** — passenger's memory flags tick up, tip/wear applied, loop repeats faster or weirder.

A shift is just this loop repeated until you either run the battery dry or head back to the Charging Room on purpose — see Power Meter for how that wrapper works.

### Power Meter (Shift Structure)

Framed like the fusion-core meter from Fallout 4's power armor, but it's what actually structures a session:

- **Passive drain** — ticks down continuously just from being active.
- **Carry drain** — burns faster while hauling a loaded tray, so heavier orders cost more charge.
- **Charging Room** — home base and shift start. Returning here on your own terms ends the shift and banks whatever tips/orders you've completed so far.
- **Running dry mid-car** — the real fail state, but a comedic one: a maintenance drone drags you back to the Charging Room, the shift ends immediately, and anything unbanked is lost.
- **The pull** — every shift comes down to "how much further can I push it before I need to turn back," which is the whole score-attack tension. No route-planning or builds required to make that decision interesting.

Charge capacity and drain rate are fixed for every player — same as every CLANKER stat, per the Design Pillar. The only thing that actually changes shift-to-shift is which **upgrades** you've earned (see Upgradable Robot Body), since those are the one system with real mechanical teeth.

### Quest Generation

Every request = **(passenger)** + **(item)** + **(complication)**, each pulled from a small pool (8-10 entries each). Small pools, mixed randomly, already produce hundreds of combos — absurdity comes from the *combination*, not from writing new content:

- A normal item + a ridiculous passenger (The Spy demanding "one (1) tap water, extremely quietly")
- A ridiculous item + a mundane complication (a sentient suitcase's snack order, delayed because the cart has a flat wheel)
- A normal item + a normal passenger + a glitch complication (the water is fine, the car it's in isn't)

### Quest Pools (Draft)

**Passengers** — signature ones from World & Passengers, plus lighter one-liners for variety:
- The Spy, The Retired Space Pirate, The Sentient Suitcase, That One Guy in the Dining Car (see World & Passengers)
- The Bridezilla-to-Be — wedding keeps relocating to a different car
- The Conspiracy Uncle — insists the train isn't actually moving, it's a treadmill
- The Overly-Formal Diplomat — represents a country that doesn't exist
- The Not-Dead Ghost — insists they're just "between stops"
- The Talking Cat — outranks literally everyone on the train and nobody questions it, orders with total imperiousness
- The Retired Superhero — treats every fetch quest like a superhero mission, over-explains accordingly

**Items:**
- A glass of water (bafflingly specific temperature/glass requirements)
- A napkin folded "correctly" — fold it however you like; whether it counts as correct is decided at random on delivery, with no actual connection to how you folded it
- A replacement monocle
- An off-menu snack they insist is on the menu
- Someone else's luggage (not theirs, wants it anyway)
- A pillow that isn't flat (impossible standard)
- Ice, but "the good kind"
- A newspaper from a day that hasn't happened yet
- A single sock, treated as a five-alarm crisis
- Decaf that's somehow "extra caffeinated"

**Complications:**
- Wrong car — the quest marker lied
- Item breaks/spills en route, improvise a substitute
- Passenger changes their mind mid-delivery
- The car glitches (sideways gravity, duplicated decor)
- Another passenger steals your tray
- The cart's out of order, forced detour
- Déjà vu — the quest marker insists you already did this one
- NPC duplication glitch — two identical passengers, conflicting requests
- Power flicker — battery takes a sudden hit
- The quest turns out to already be complete when you arrive, but delivering anyway is still required

### Delivery Resolution

Whatever you actually deliver — dead-on correct or a nonsense substitute — there's a flat ~5% chance the outcome flips: a perfect delivery reads as a failure, or a wrong delivery reads as correct. Ties straight back into the Design Pillar: even the one moment that looks skill-based (did I bring the right thing?) isn't fully trustworthy, so players can never be 100% sure effort was what decided the outcome.

### Passenger Memory

No branching writing required — passengers just track a couple of numeric flags (times served, last outcome). Their request pool and non-dialogue reaction lines shift slightly based on those flags, so repeat visits feel like they "remember" you even though nothing was actually scripted per-passenger.

## Upgradable Robot Body

Unlike your CLANKER build, these are real, earned mid-game (bought with tips or found as loot), and actually change how a shift plays — the one system in the game where a "choice" has genuine mechanical effect:

- Better legs — faster traversal, lower passive drain
- Extra arms — carry more trays/items at once, reduces carry-drain penalty
- Sarcasm module — unlocks snarkier non-dialogue flavor lines (still cosmetic, matches the joke)

## Tech (Godot)

**Engine**: Godot 4.x (per README). None of the above pushes past what Godot handles well out of the box:

- **First-person movement** — `CharacterBody3D` + the standard first-person controller pattern.
- **Tray-balancing mechanic** — leaning toward a "faked" physics feel: script-driven tilt/spring reacting to velocity and turns, with a spill threshold, rather than a fully simulated `RigidBody3D` on a joint. Easier to tune for *fun* than for *realism*.
- **Procedural car shuffling** — modular scene instancing/streaming as the player moves; no exotic tooling needed.
- **Non-dialogue system, Power Meter, Passenger Memory, Quest Pools** — plain GDScript state: an autoload singleton for global/shift stats, arrays or `Resource` files for the pools, `RandomNumberGenerator` for combos and the Delivery Resolution flip. The easiest part of the project, engine-wise.
- **Glitch VFX** (car glitches, NPC duplication, sideways gravity) — Godot's shader language / visual shader editor; well-trodden ground for "corrupted geometry" style effects.

**Expected hard parts** (feel/tuning, not engine limitations): getting the tray-balance mechanic satisfying rather than annoying, and making car-to-car streaming seamless enough that the "endless train" illusion holds up.

## Extra Acronym

- **B**umbling
- **E**xecutives
- **T**rying
- **H**opelessly,
- **E**ndangering
- **S**tory-
- **D**riven
- **A**dventures
