+++
title = "Oathbreaker: Creating the Night"
draft = false
date = 2023-02-09
template = "blog.html"
+++

# Oathbreaker: Creating the Night

I'm nearly done with the first iteration of
[Oathbreaker's](https://github.com/kiedtl/roguelike) first faction, which I had
planned for some months now but only recently found to time to implement.

Introducing: the Night Creatures.

![Player attacked by Night Creatures](//tilde.team/~kiedtl/images/rl/night/running-harried-by-nc.png)

Unlike the other enemies you'll face while trying to escape the Dungeon, the
night creatures are collectively neutral to both you and your enemies. They only
becoming hostile if you trespass on their *lairs*, special areas that appear on
most levels.

![Lair screenshot](//tilde.team/~kiedtl/images/rl/night/lair.png)

And why would you trespass on their lairs?

## Trespassing: the perks

The answer, as is typical of roguelikes, is to get more shiny loot.

Although you should be able to survive just fine without raiding lairs, doing so
can net several types of rare potions and evocables, as well as unique Lair-only
equipment:

- Firstly, there are the **shadow weapons**: the shadow mace, shadow sword, and
  shadow maul. All confer special effects on your foes if you succeed against
  their willpower and if both you and your foe is standing in a dark area:
  shadow swords send your opponent insane, shadow maces paralyse all foes in
  your line of sight for a brief duration (buying time to escape), and shadow
  mauls create a spectral clone of your foe (that is usually neutral to you, but
  will be hostile if you've angered the night creatures).
- There's also **shadow armor**, which are generally worse compared to their
  non-shadow counterparts until you stand in a dark area, when the benefits
  become much better.
- The **ethereal shield** gives *negative* evasion, but will push foes backwards
  on a dodged attack if a will-check succeeds and the foe is in a dark area.
- **Fuming vests** emit a small amount of smoke whenever you move, allowing you
  to quickly get out of foe's line-of-sight.

Finally, there are two Lair-only rings.

The **Ring of Excision** spawns a spectral sword, which pierces enemies in a line
whenever you move in the direction you moved.

![GIF showcasing the excision ring](//tilde.team/~kiedtl/images/rl/night/excision.gif)

The **Ring of Conjuration** spawns a few volleys of spectral sabres, which simply
attack any enemies that you can see and then vanish when there are no more
enemies in sight. The number of sabres in a volley is dependent on your
`Conjuration` stat, which starts out at 2 and can be increased by wearing
*spectral equipment* (spectral crowns, spectral cloaks, spectral vests, etc),
another Lair-only speciality.

![GIF showcasing the conjuration ring](//tilde.team/~kiedtl/images/rl/night/conjuration.gif)

Moreover, by finding *spectral orbs* in lairs, you can gain a number of
Conjuration augments that modifies the spectral sabre's stats or introduces new
abilities:

- **Wall disintegration** augments cause 1-3 adjacent walls to disintegrate into
  a single sabre while there are other allied sabres in sight.
- **Fire resistance** and **electricity resistance** provide up to 75% fire and
  electricity resistance, respectively.
- **Undead bloodthirst** causes a new volley of spectral swords to spawn nearby
  whenever you see a hostile undead perish.
- **Melee** and **evasion** augments provide extra to-hit and evasion bonuses,
  respectively.

Conjuration rings start out fairly weak (two spectral swords with 1 HP and
mediocre stats can barely kill or distract a single guard, let alone several),
making them more of an auxiliary strategy than a powerful item to build around.
However, if one chooses to continue raiding lairs and collect spectral equipment
and conjuration augments, the Conjuration ring can become extremely powerful --
what's not to like about an ability that can summon 6 evasive enemies each turn,
and then create more just by moving near walls? The swords are still just as
fragile, of course, but by the time that patrol squad has killed them all a
skilled player will be on the other side of the map.

## Trespassing: the consequences

Obviously, the night creatures aren't going to sit around while one breaks down
their barricades and steals their things. Thus, raiding lairs carries both short
and long-term consequences.

The short term consequence: the night creatures within the lair, if there are
any, become angry. And an angry night creature is easily one of the most
dangerous creatures you'll ever meet in the early-to-mid game.

![GIF showcasing the conjuration ring](//tilde.team/~kiedtl/images/rl/night/death.png)

The good news is that you can pacify them simply by moving off their turf.

However, whenever you break into a lair you'll lose 2 *reputation*, an unique
stat that begins at 0 and decreases as you raid more lairs.

At -5 reputation, night creatures remain hostile to you even if you're not
trespassing. (This can be seen in the above screenshot on the HUD's top.)

At -10 reputation, you'll very rarely find that a night creature has stormed out
of its lair specifically to hunt you down and exact revenge. Oops.

This would be a bit difficult, especially for players with the ring of
conjuration (since they'll typically want to visit multiple lairs in hopes of
finding spectral equipment or spectral orbs). But as you reach new floors and
move away from the lairs you've raided, your reputation goes up by 1, enabling
incorrigible robbers to listen to the piper's tune for a bit longer before
they'll have to pay him.

## The night creatures

But these night creatures themselves -- what exactly are they? Demons? Nature
guardians? Ghosts of previous players?

The answer is complicated, and explaining it would require divulging much of the
game's in-universe lore. Although it's not possible to find that lore yet
in-game, eventually I'd like to do something similar to Cogmind and allow
players to find manuscripts and such in special branches, which would describe
the game's backstory and lore. For that reason, I don't want to discuss their
lore here in any way.

There are currently four night creatures, with three more planned for a later
expansion.

**Spectral totems** are stationary enemies that overwhelm enemies by conjuring
spectral swords.

**Night reapers** are highly competent warriors wielding shadow mauls, which as
mentioned create spectral clone of enemies.

**Grues** emit a special insanity-inducing gas when wounded, as well as causing
retaliatory Spikes damage when attacked.

**Slinking terrors** are spectral monstrosities, able to attack up to 6 times in
a single turn. They always stay near walls, never moving into open space.

With one exception, the night creatures are only found in lairs, minding their
own business and hoping that you'll mind yours. Rarely, you'll see them
traveling across the map to visit another lair, on which occasions they'll use a
special *Mass Amnesia* ability to dispose of inquisitive guards and patrols.

![Night Reaper fending off enemies while player looks on](//tilde.team/~kiedtl/images/rl/night/amnesia.gif)

## Aligning with the Night

The exception to this is a special encounter on 7/Prison (the second floor from
the player's starting point), where you can meet a lone Night Reaper locked in a
cell. When you show up, he'll ask you to let him out.

![Player finding the Night prisoner and releasing it](//tilde.team/~kiedtl/images/rl/night/prisoner.gif)

If you oblige (by breaking down the cell's door, as seen in the GIF), he'll
thank you (*"I appreciate it."*) and go on his way back to a nearby lair. At
this point you'll notice that your reputation is now *positive*, signifying that
you've aligned yourself with the Night.

Aligning with the Night has two main consequences:

- You get free access to the Night's lairs and the shinies within, without fear
  of reprisal.
- You cannot use any item that creates light or fire, which includes
  flamethrowers, eldritch lanterns, potions of incineration and decimation, and
  the rings of cremation and damnation. "Evil" rings are also off-limits, which
  rules out the ring of insurrection (which summons allied undead). In other
  words, you're locked out of many of the most valuable emergency buttons.

Admittedly, aligning with the Night is currently the most optimal choice,
because there are many immediate and strong benefits to doing so (free potions
of petrification!). Eventually, though, I'd like for Night-aligned builds to be
as difficult or, for tackling the extended game, *more difficult* than unaligned
builds.
