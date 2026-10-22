---
Fraktion: Horde
Klasse: Schamane
Level: 70
Thema: Azeroth
---
Every feature of the **Azeroth** theme on one page. Each section shows the result first, then the markdown that produces it. Open it in reading view for the full effect.

> [!tip] Theme settings
> Faction (Neutral / Alliance / Horde), parchment pages in dark mode, link color, brackets and ornaments live under **Settings → Style Settings → Azeroth**.

---

## Headings

# Quest title (H1)
## Section (H2)
### Subsection (H3)
#### Item name (H4)
##### Small caps (H5)
###### Smallest (H6)

```md
# Quest title (H1)
## Section (H2)
```

---

## Links and text

Internal links read like chat links: [[Kräuter AZEROTHS]] or [[Azeroth Theme Showcase#Callouts|a heading]]. Links to notes that don't exist yet turn "poor" grey, and external links like the [wowhead database](https://www.wowhead.com) are legendary orange.

**Bold is white highlight text**, *italic stays calm*, `inline code` is artifact gold, and ==highlights== glow softly.

> "The land is dying, and we are all that stands between it and the Burning Legion."
> — Thrall

Item and class colors inline: <span class="q-poor">[Poor]</span> <span class="q-uncommon">[Uncommon]</span> <span class="q-rare">[Rare]</span> <span class="q-epic">[Epic]</span> <span class="q-legendary">[Legendary]</span> · <span class="c-shaman">Schamane</span> <span class="c-druid">Druide</span> <span class="c-deathknight">Todesritter</span>

```html
<span class="q-epic">[Ashkandi]</span>   q-poor … q-heirloom
<span class="c-mage">Jaina</span>         c-warrior, c-paladin, c-hunter, c-rogue, c-priest,
                                         c-deathknight, c-shaman, c-mage, c-warlock,
                                         c-monk, c-druid, c-demonhunter, c-evoker
```

---

## Tags

#episch #legendär #selten #Schamane #Krieger #Magier #Horde #Allianz

Quality tags (#poor … #heirloom, German: #schlecht #verbreitet #selten #rar #episch #legendär #artefakt #erbstück), class tags in English or German, and #alliance / #allianz / #horde glow in their color. Every other tag is a gold label.

---

## Lists and quest objectives

- Collect 8 Peacebloom
- Slay the Razormane quilboars
	- Nested objective
1. Accept the quest
2. Ride to the Crossroads

- [ ] Open objective
- [x] Completed objective
- [!] Quest available
- [?] Ready to turn in
- [-] Abandoned quest

```md
- [!] Quest available
- [?] Ready to turn in
- [-] Abandoned quest
```

XP bar: <progress value="62" max="100"></progress>

```html
<progress value="62" max="100"></progress>
```

---

## Callouts

> [!quest] The Barrens Herb Run
> Collect herbs for the elders. Peacebloom grows near water; Silverleaf likes the shade.
> - [ ] 0/8 Peacebloom
> - [x] 5/5 Silverleaf

> [!turnin] Report to Elder Bloodhoof
> You have everything he asked for.

> [!gossip] Innkeeper Pala
> Welcome, traveler. A warm bed and a hot meal for a few coins?

```md
> [!quest] Title          (or [!questlog])
> [!turnin] Title         (or [!complete])
> [!gossip] NPC name
```

> [!item|epic] Ashkandi, Greatsword of the Brotherhood
> Binds when picked up
> Two-Hand · Sword
> 172 - 259 Damage
> ==Equip: Increases attack power by 86.==
> *"A massive blade, still warm from the forge."*
> ~~Requires level 60~~

```md
> [!item|epic] Item name
> ==green effect line==
> *gold flavor text*
> ~~red requirement~~
```
Quality after the `|`: poor, common, uncommon, rare, epic, legendary, artifact, heirloom (German names work too).

> [!boss] Ragnaros
> Avoid **Wrath of Ragnaros**; tanks swap at 3 stacks.

> [!loot] Reward
> 12 gold, 40 silver and a guild tabard.

> [!achievement|10] Molten Core
> Defeat Ragnaros in Molten Core.

> [!alliance] For the Alliance
> Stormwind stands.

> [!horde] For the Horde
> Lok'tar ogar!

```md
> [!boss] Name            (or [!raid], [!encounter])
> [!loot] Title           (or [!reward])
> [!achievement|10] Name  the number becomes the points shield
> [!alliance] / [!horde]
```

> [!epic] Quality callouts
> `[!poor]` `[!common]` `[!uncommon]` `[!rare]` `[!epic]` `[!legendary]` `[!artifact]` `[!heirloom]`

The standard callouts use the item-quality colors:

> [!info] Info
> Rare blue.

> [!warning] Warnstufe: Vorsicht
> Legendary orange.

> [!danger] Warnstufe: Aufsichtspflichtig
> Error red.

---

## Chat lines

> [!say] Kev
> Ihr seht müde aus, Freundin.

> [!yell] Thrall
> Für die Horde!

> [!whisper] Yune
> Treffen wir uns später am Brunnen?

> [!party] Seb
> Bereit für den Pull?

> [!guild] Elvira
> Wer hat noch Friedensblumen übrig?

> [!emote] Kev
> lehnt sich an den Tresen und grinst.

> [!system] System
> Ihr habt die Quest abgeschlossen.

```md
> [!say] Name
> Text
```
Channels: say, yell, whisper, party, guild, officer, emote, system, npc.

---

## Chat log notes

Add this to the properties of an RP log and the whole note renders like the chat frame, with `*actions*` in emote orange:

```yaml
cssclasses: chatlog
```

---

## Table and code

| Item | Quality | Drop chance |
| --- | --- | --- |
| <span class="q-legendary">[Thunderfury]</span> | Legendary | 0.4% |
| <span class="q-epic">[Ashkandi]</span> | Epic | 12% |
| <span class="q-rare">[Ravager]</span> | Rare | 18% |

```js
// Summon the raid
function summon(raid, target) {
  const count = raid.members.length;
  return `Summoning ${count} heroes to ${target}`;
}
```
