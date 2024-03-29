<style>
/* GLOBAL FORMATTING  */

  /* Resize page to international A4 */
  .phb {
    width: 210mm;
    height: 296.8mm;
    background-image: url('https://www.gmbinder.com/images/RVaHjr8.png');
    background-size: cover;
  }
  .phb:after { content: ""; }


/* FRONT PAGE STYLES */

  .cover-header-container {
    display: block;
    position: absolute;
    width: 100%;
    top: 80px;
    left: 0;
    right: 0;
    clear: both;
  }

  .cover-header-logo {
    display: block;
    width: 700px;
    margin: auto;
  }

  .cover-header-divider {
    display: block;
    width: 580px;
    margin: -12px auto -6px;
  }

  .cover-header-title {
    display: block;
    width: 700px;
    margin: auto;
    color: white;
    font-family: NodestoCaps,nodesto,sans-serif;
    font-weight: normal;
    font-size: 72px;
    line-height: 72px;
    text-align: center;
    text-shadow: 2px 2px 4px #000, -2px 2px 4px #000, 2px -2px 4px #000, -2px -2px 4px #000;
  }

  .cover-footer-container {
    display: block;
    position: absolute;
    width: 100%;
    bottom: 28px;
    left: 0;
    right: 0;
    clear: both;
  }

  .cover-footer-subtitle,
  .cover-footer-version {
    display: block;
    width: 500px;
    margin: auto;
    color: white;
    font-family: NodestoCaps,nodesto,sans-serif;
    font-weight: normal;
    text-align: center;
    text-shadow: 1px 1px 2px #000, -1px 1px 2px #000, 0px 0px 2px #000;
  }
  .cover-footer-subtitle {
    font-size: 28px;
    line-height: 28px;
  }
  .cover-footer-version {
    margin-top: 16px;
    font-size: 20px;
    line-height: 20px;
  }

/* TABLE OF CONTENTS  */

  /* toc specifically wants black text. This resets the headers*/
  .toc a {
    color: inherit !important;
  }
  /* Allow dot leaders to fill remaining space but not overlap */
  .toc li span:nth-child(2) {
    width: auto;
    overflow: hidden;
    white-space: nowrap;
    display: block;
  }
  .toc li span:nth-child(2):after {
    font-family: BookSanity;
    font-size: 0.317cm;
    font-weight: normal;
    color: black;
    content:
      " ........................................"
      "........................................."
      ".........................................";
    }

  /* Style TOC page numbers*/
  .toc li span:first-child {
    float: right;
    font-family: BookSanity;
    font-size: 0.317cm;
    font-weight: normal;
    color: black;
    margin-left: 1px;
  }

  /* Adjust TOC H3 styles */
  .toc li h3 span:nth-child(2):after {
    content: " ";
  }
  .toc li h3 {
    margin-bottom: 4px !important;
    margin-top: 10px !important;
    line-height: initial !important;
  }
  .toc li h3 span:first-child {
    line-height: 1.8em !important;
  }

  /* Reduce TOC list indentation*/
  .toc ul ul {
    margin-left: 10px !important;
  }
  .toc>ul>li {
    margin-bottom: initial !important;
  }


/* TABLES AND BLOCKS */

  /* Adjust tables */
  table tr:nth-child(odd) td { background-color: #FFF0f5; }
  .phb hr+section blockquote tr:nth-child(odd) td { background-color: transparent; }

  /* Clear internal padding and add gap above for green note blocks*/
  .phb blockquote {
    padding-left: 0px;
    padding-right: 0px;
  }
  .phb blockquote { margin-top: 1em; }

  /* Clear internal padding in creature statblocks */
  .phb hr+section blockquote {
    padding-left: 0px;
    padding-right: 0px;
  }

  .phb blockquote {
    box-shadow: 1px 4px 14px rgba(0,0,0,0.42);
  }

  /* For creature statblocks within range (start and end must be specified),
     don't show a background. Used for the appendix creatures */
  .phb:nth-of-type(n+116):nth-of-type(-n+150) hr+section blockquote {
    background: none;
    border: none;
    box-shadow: none;
    margin-top: 12px;
    margin-bottom: 12px;
    padding-top: 6px;
    padding-bottom: 6px;
  }

  /* For double-wide creature statblocks that we want to have anchored to the
  bottom of the page regardless of content flow. */
  .statblock-bottom-wide {
    position:absolute;
    bottom:63px;
    right:1.7cm;
    left:1.7cm;
    margin-top:1200px;
  }


/* FOOTER */

  /* Footnotes */
  .phb .pageNumber {
    color: #7e735c;
    z-index: 1000;
  }
  .phb .footnote { color: #7e735c; }

  /* On odd pages before the bestiary, have just the page tear */
  .phb:nth-child(odd):nth-of-type(n+2):after {
    content: '';
    height: 125px;
    background-image: url(https://www.gmbinder.com/images/PB8On0U.png), url('https://gmbinder.com/images/YWardeu.png');
    background-size: 120px 120px, 816px 55px;
    background-repeat: no-repeat, no-repeat;
    background-position: bottom right -10px, bottom;
  }

  /* Reversed for alternating pages */
  .phb:nth-child(even):nth-of-type(n+2):after {
    content: '';
    height: 125px;
    background-image: url(https://www.gmbinder.com/images/PB8On0U.png), url('https://gmbinder.com/images/YWardeu.png');
    background-size: 120px 120px, 816px 55px;
    background-repeat: no-repeat, no-repeat;
    background-position: bottom right -10px, bottom;
    -webkit-transform: scaleX(-1);
    transform: scaleX(-1);
  }

  /* On odd bestiary pages, have the Monster Manual page tear and lettering */
  .phb:nth-child(odd):nth-of-type(n+0):nth-of-type(-n+115):after {
    content: '';
    height: 125px;
    background-image: url(https://gmbinder.com/images/lLWeevR.png), url('https://gmbinder.com/images/YWardeu.png');
    background-size: 120px 120px, 816px 55px;
    background-repeat: no-repeat, no-repeat;
    background-position: bottom right -10px, bottom;
  }

  /* Reversed for alternating pages */
  .phb:nth-child(even):nth-of-type(n+0):nth-of-type(-n+115):after {
    content: '';
    height: 125px;
    background-image: url(https://gmbinder.com/images/lLWeevR.png), url('https://gmbinder.com/images/YWardeu.png');
    background-size: 120px 120px, 816px 55px;
    background-repeat: no-repeat, no-repeat;
    background-position: bottom right -10px, bottom;
    -webkit-transform: scaleX(-1);
    transform: scaleX(-1);
  }

  /* The page number position */
  .phb .pageNumber {
    right: 0px;
  }

  /* The page number position for alternating pages */
  .phb:nth-child(even) .pageNumber {
    left: 0px;
  }

  /* The letter in the Monster Manual page tear */
  .pageLetter {
    position: absolute;
    right: 15px;
    bottom: 87.5px;
    color: #905727;
    z-index: 1000;
    font-size: 135%;
  }

  /* Reversed for alternating pages */
  .phb:nth-child(even) .pageLetter {
      left: 15px;
  }


/* MONSTER MANUAL LETTER SECTION HEADER */

  /* Adds the surrounding framing for the big, bold monster letter headings */
  .letterheader {
    position: absolute;
    top: 30px;
    left: 0;
    right: 0;
    margin-left: auto;
    margin-right: auto;
    background-image: url(https://gmbinder.com/images/YH3aESG.png);
    background-size: cover;
    width: 775px;
    height: 133px;
  }

  /* Base component for the actual letter in the heading */
  .mmletter {
      position: absolute;
      top: 20px;
      left: 0;
      right: 0;
      margin-left: auto;
      margin-right: auto;
      background-size: cover;
      width: 163.2px;
      height: 163.2px;
  }

  /* Use one in combination with .mmletter to show that letter */
  .mml-a { background-image: url(https://gmbinder.com/images/fVVv93s.png); }
  .mml-b { background-image: url(https://gmbinder.com/images/21X6N0B.png); }
  .mml-c { background-image: url(https://gmbinder.com/images/MvnpOWF.png); }
  .mml-d { background-image: url(https://gmbinder.com/images/AFbLU4P.png); }
  .mml-e { background-image: url(https://gmbinder.com/images/28NVNf9.png); }
  .mml-f { background-image: url(https://gmbinder.com/images/Oyrhmqy.png); }
  .mml-g { background-image: url(https://gmbinder.com/images/fRyiQn4.png); }
  .mml-h { background-image: url(https://gmbinder.com/images/N8NamlT.png); }
  .mml-i { background-image: url(https://gmbinder.com/images/xWI93aa.png); }
  .mml-j { background-image: url(https://gmbinder.com/images/GgIzsun.png); }
  .mml-k { background-image: url(https://gmbinder.com/images/OcObsWl.png); }
  .mml-l { background-image: url(https://gmbinder.com/images/B7AUyR6.png); }
  .mml-m { background-image: url(https://gmbinder.com/images/q4wXoxt.png); }
  .mml-n { background-image: url(https://gmbinder.com/images/OJtC4w9.png); }
  .mml-o { background-image: url(https://gmbinder.com/images/adeRr5d.png); }
  .mml-p { background-image: url(https://gmbinder.com/images/EEhcrSR.png); }
  .mml-q { background-image: url(https://gmbinder.com/images/O1AhfzL.png); }
  .mml-r { background-image: url(https://gmbinder.com/images/w66eIuZ.png); }
  .mml-s { background-image: url(https://gmbinder.com/images/YEoe0PP.png); }
  .mml-t { background-image: url(https://gmbinder.com/images/7Bk9D35.png); }
  .mml-u { background-image: url(https://gmbinder.com/images/uVJZYUg.png); }
  .mml-v { background-image: url(https://gmbinder.com/images/gKjngey.png); }
  .mml-w { background-image: url(https://gmbinder.com/images/14WWpsC.png); }
  .mml-x { background-image: url(https://gmbinder.com/images/ojIYjh0.png); }
  .mml-y { background-image: url(https://gmbinder.com/images/Gi1ePwY.png); }
  .mml-z { background-image: url(https://gmbinder.com/images/0ZTFNVs.png); }


/* INK BLOT STYLES */

  /* Root style for inkblots. Use alone, or together with
  one of the inkb lotstyle classes below. Essentially:
  <img url='{url}' class='inkblot inkblot-blue' />
  */
  .inkblot {
    position: absolute;
    mix-blend-mode: multiply;
    opacity: 0.6;
  }

  .inkblot-blue {
    filter: hue-rotate(190deg) saturate(120%)
  }

  .inkblot-green {
    filter: hue-rotate(120deg)
  }

</style>

<div style='margin-top:130px;'></div>

# Dinosaurs
Dinosaurs are among the oldest reptiles in the world, ancient in every sense of the word. Their presence can inspire both awe and dread into any adventurer fortunate -- or unfortunate -- enough to cross their path. They roam far and wide across Azeroth; all the way from remote mountain valleys, to humid jungles, and to rugged barren plains. 

***Feared and Revered.*** Some of Azeroth's denizens, trolls in particular, revere dinosaurs. Several of the primal Loa take the appearance of a dinosaur, such as the devilsaur Loa Rezan and the direhorn Loa Torcali. 

For the Zandalar tribe, it is a rite of passage to venture away from home, into the wilds, in order to steal or subdue a beast. Any beast would do for such trials, but a wild dinosaur is a prized claim.

***Giants Among Beasts.*** Dinosaurs come in many sizes and shapes, some absolutely tremendous, featuring a wide variety of markings and colorations. They primarily split into two groups: savage, territorial predators, and docile yet still undeniably dangerous herbivores.

### Ankylodon
The ankylodon is a broad, low-slung dinosaur, native to Zandalar. It is kept up by its powerful limbs, and almost every part of its body, save for the belly, is decked with hardened plates. Long spikes protrude from these plates; <br>a characteristic appearance that has flocks of ankylodons sometimes referred to as "thornhides". It is a herbivore, preferring to graze on ferns and low shrubs, shearing them off with its beak-like upper jaw.

### Brutosaur
Brutosaurs are enormous, even among dinosaurs. They have small heads and incredibly long necks, relative to the rest of their body, and move along at a lumbering pace with their pillar-like legs. Despite their imposing stature, bruto&shy;saurs are known to be very docile unless threatened. They are omnivores, yet most appear to have an exclusively herb&shy;ivorous diet, rarely ever hunting meat of their own volition.

### Devilsaur
This giant lizard stands tall on its two powerful hind legs, with two stunted forelimbs stretched out before it. The devilsaur takes its name from its utterly savage attacks, as it tackles its prey down with immense force before tearing it limb from limb. Despite its ferocity, the devilsaur's massive size has many hunters seeking the beast out for its hide, which is both supple and extraordinarily tough. Devilsaurs may grow well above thirty feet, weighing in at almost sixteen tons. 

Female devilsaurs tend to be smaller and lighter, though they are even more aggressive than their male counterpart. During mating seasons, once the nest has been made and her eggs have been laid, she will leave it to the male who fathered the clutch to protect them until they hatch.

<div class='letterheader'></div>
<div class="mmletter mml-d"></div>
<div class="pageLetter">D</div>
<div class='footnote'>DINOSAURS </div>

<img src='https://www.gmbinder.com/images/din7hXr.jpg' style='position:absolute; top:0px; right:-750px; width:2020px' />
<img src='https://www.gmbinder.com/images/7drSEMn.png' style='position:absolute; top:0px; right:-15px; width:900px' />

\pagebreakNum

### Diemetradon
The diemetradon—one of the strongest predators in the Un'Goro Crater—is recognized for the two enormous, jag&shy;ged crests protruding from its back. Its legs are squat and strong, for which it is far from the fastest dinosaur, though its body is decked in plate-like scales able to withstand tremendous force. When a diemetradon fights or hunts, it is known to simply lumber dead ahead against its target; rushing in to pin them down against a tree or in a swamp.

It is said that the diemetradon's howl is deafening, like a thundering boom capable of drowning out most other sounds around it.

### Direhorn
Direhorns are three-horned saurian titans known to popu&shy;late many islands throughout the South Seas. They are especially prominent on Zandalar, the Isle of Giants and the Isle of Thunder. They may seem like gentle giants at first, though they are among the toughest and strongest animals to walk on Azeroth. Even juvenile direhorns have been known to wreak utter havoc on unsuspecting victims. 

### Pterrordax
Tall as a horse and weighing up to 1,500 pounds, the pterrordax's keen senses guides it along as it soars through the air in search for fresh meat. Its claw-tipped wings are utterly tremendous, and its beak-like snout is lined with razor-sharp teeth. The pterrordax prefers to hunt alone, swooping down on unsuspecting prey from above to batter it to death with its wings before proceeding to tear flesh from bone. It is a solitary hunter, and adventurers' accounts of multiple have mainly been during mating season: a two-week period during early spring-time.

If their breeding grounds are threatened, otherwise lone pterrordax are quick to band together in large flights to fend off attackers. Afterwards, they disband just as quickly.

A pterrordax's pigmentation ranges from bright mossy greens to deep emerald hues, with brightly shining eyes. Closely related to the pterrordax is the even more terrifying pterrorwing—also known as Skyscreamer. It is massive in comparison, and stands out for the large sail on its snout.

### Raptor
The raptor is a large, aggressive dinosaur, known far and wide for its strength and immense speed. Out in the open, it is near impossible to outrun its leaping stride, and once it has caught up to its prey it pounces; driving its hooked talons in deep.

Even among dinosaurs, raptors are exceptionally intelli&shy;gent. Their packs act closer to colonies, with established hierarchies and and breeding grounds that could be mis&shy;taken for settlements when viewed from afar. They are very visually striking creatures, decked in scales and feathers ranging from bright blue and white, to striking red and orange, to deep black, purple, and green. 

### Sabertusk
Little is known about the enigmatic sabertusk, other than its nativity to Zandalar and occasional sightings on other, smaller islands nearby.  Though unwary adventurers have occasionally mistaken it for other land-dwelling reptiles, the sabertusk is visibly striking for the long and heavy tusks protruding from its maw. Its legs are long and its tail is narrow, with tall and coarse spikes running the length of its spine; all the way up to a prominent horn on its snout. 

\columnbreak

### Saurid
Saurid are small bipedal dinosaurs native to Zandalar, known for their nimble grace and venomous bite. The Zandalari trolls consider the saurid to be vermin, no better than rats, as they frequently steal food, poison waters, and prey on children and on the wounded.

However, when Zandalar renewed their alliance with the mogu at the Isle of Thunder, they brought the saurid with them to train. There, the tiny critters proved an immensely valuable weapon in the trolls' arsenal, let out loose in the wilds to hunt in the night.

### Stegodon
Stegodons are large herbivorous dinosaurs, whose massive bodies are heaved along on legs the size of tree trunks. They are notorious for their short temper and alarmingly aggressive turns, often attacking trespassers on sight as they patrol their territories. An enormous horn extends from the stegodon's snout, and spike-like plates run like a jagged fin across the length of its spine, over a back decked in hardened scales. Most stegodons have skin in dark shades of green, though some grow paler and grittier hues.

### Threshadon
The threshadon is a marine dinosaur, whose compact body is driven by a set of powerful flippers. Much like a bruto&shy;saur, its neck accounts for a third of its total length, and is able to flex and twist in whichever direction it needs to dig around muddy lake-beds and pull branches from riversides.

Though they are herbivores first and foremost, grazing threshadon herds are notorious for how fast they tear through and and all plant life within reach—before migrat&shy;ing on to new grounds. When a herd has found a grazing spot, the threshadons defend it aggressively. Any other creatures they encounter are attacked on sight. When it fights, the threshadon uses its long neck to lunge at its target, dealing devastating blows with rows of long, jagged teeth. Its jaws are strong enough to crush armor and snap bones, and it is not unusual for it to consume it kills whole.

___
> ## Ankylodon
> *Large beast, unaligned*
> ___
> - **Armor Class** 16 (natural armor)
> - **Hit Points** 52 (7d10 + 14)
> - **Speed** 30 ft.
> ___
> STR | DEX | CON | INT | WIS | CHA
>|:---:|:---:|:---:|:---:|:---:|:---:|
> 19 (+4)|11 (+0)|15 (+2)|2 (-4)|12 (+1)|5 (-3)|
> ___
> - **Damage Resistances** poison; bludgeoning, piercing, and slashing from nonmagical attacks
> - **Senses** passive Perception 11
> - **Languages** —
> - **Challenge** 4 (1,100 XP)
> ___
>
> ### Actions
> ***Claws.*** *Melee Weapon Attack:* +6 to hit, reach 5 ft., one target. *Hit:* 22 (4d8+4) piercing damage.<!-- https://wc5e-cr-calculator.frogvall.com/?0;16;52;6;12;22;0;0;0;0;0;0;0;0;0;0;0;1;;;;3;;;;;;;;;;1;;;;;;;;10;;;;;; -->

<div class="pageLetter">D</div>
<div class='footnote'>DINOSAURS </div>

\pagebreakNum

<div style='margin-top:530px;'></div>

___
> ## Brutosaur
> *Gargantuan beast, unaligned*
> ___
> - **Armor Class** 12 (natural armor)
> - **Hit Points** 162 (12d20 + 36)
> - **Speed** 30 ft.
> ___
> STR | DEX | CON | INT | WIS | CHA
>|:---:|:---:|:---:|:---:|:---:|:---:|
> 21 (+5)|9 (-1)|17 (+3)|2 (-4)|10 (+0)|7 (-2)|
> ___
> - **Saving Throws** Con +6
> - **Senses** passive Perception 10
> - **Languages** —
> - **Challenge** 6 (2,300 XP)
> ___
>
> ### Actions
> ***Stomp.*** *Melee Weapon Attack:* +8 to hit, reach 20 ft., one target. *Hit:* 36 (7d8 + 5) bludgeoning damage, and the target must succeed on a DC 16 Strength saving throw or be knocked prone.
>
> ***Tail.*** *Melee Weapon Attack:* +8 to hit, reach 20 ft., one target. *Hit:* 32 (6d8 + 5) bludgeoning damage. If the target is a creature, it must succeed on a DC 15 Strength saving throw or be pushed up to 30 feet away from the brutosaur and knocked prone.<!-- https://wc5e-cr-calculator.frogvall.com/?1;12;162;8;12;36;0;0;0;0;0;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;;;;;;;;10;;;;;; -->

\columnbreak

<div style='margin-top:249px;'></div>

___
> ## Devilsaur
> *Huge beast, unaligned*
> ___
> - **Armor Class** 13 (natural armor)
> - **Hit Points** 136 (13d12 + 52)
> - **Speed** 50 ft.
> ___
> STR | DEX | CON | INT | WIS | CHA
>|:---:|:---:|:---:|:---:|:---:|:---:|
> 25 (+7)|10 (+0)|19 (+4)|2 (-4)|12 (+1)|9 (-1)|
> ___
> - **Skills** Perception +4
> - **Senses** passive Perception 14
> - **Languages** —
> - **Challenge** 8 (3,900 XP)
> ___
>
> ### Actions
> ***Multiattack.*** The devilsaur makes two attacks: one with its bite and one with its tail. It can't make both attacks against the same target.
>
> ***Bite.*** *Melee Weapon Attack:* +10 to hit, reach 10ft., one target. *Hit:* 39 (5d12 + 7) piercing damage. If the target is a Medium or smaller creature, it is grappled (escape DC 17) . Until this grapple ends, the target is restrained, and the devilsaur can't bite another target.
>
> ***Tail.*** *Melee Weapon Attack:* +10 to hit, reach 10ft., one target. *Hit:* 25 (4d8 + 7) bludgeoning damage. If the target is a creature, it must succeed on a DC 17 Strength saving throw or be pushed up to 10 feet away from the devilsaur and knocked prone.
>
> ***Maim.*** One creature grappled by the devilsaur's bite takes 59 (8d12 + 7) piercing damage. If this reduces the creature to 0 hp, the devilsaur swallows it and the grapple ends. While swallowed, the creature is blinded and restrained, it has total cover against attacks and other effects outside the devilsaur, and it takes 10 (3d6) acid damage at the start of each of the devilsaur's turns.
> If the Devilsaur takes 20 damage or more on a single turn from creatures inside it, it must succeed on a DC 15 Constitution saving throw at the end of that turn or regurgitate all swallowed creatures, which fall prone in a space within 10 feet of it. If the devilsaur dies, a swallowed creature is no longer restrained by him and can escape from the corpse using 15 feet of movement, exiting prone. 
>
><!-- https://wc5e-cr-calculator.frogvall.com/?1;13;136;10;12;39;25;0;0;0;0;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;;;;;;;;10;;;;;;-->

<div class="pageLetter">D</div>
<div class='footnote'>DINOSAURS </div>

<img src="https://www.gmbinder.com/images/tiU4RnD.png" class="inkblot" style="top:-100px; right:0px; width:800px; transform:rotate(90deg)">
<img src='https://www.gmbinder.com/images/DOHKZPb.png' style='position:absolute; top:0px; right:0px; width:1200px' />

\pagebreakNum

<div class='statblock-bottom-wide'>

___
___
> ## Devilsaur King
> *Huge beast, unaligned*
> ___
> - **Armor Class** 15 (natural armor)
> - **Hit Points** 187 (15d12 + 90)
> - **Speed** 50 ft.
> ___
> STR | DEX | CON | INT | WIS | CHA
>|:---:|:---:|:---:|:---:|:---:|:---:|
> 29 (+9)|12 (+1)|22 (+6)|2 (-4)|12 (+1)|15 (+2)|
> ___
> - **Skills** Intimidation +6, Perception +6, Stealth +6
> - **Senses** passive Perception 16
> - **Languages** —
> - **Challenge** 14 (11,500 XP)
> ___
>
> ***Legendary Resistance (1/Day).*** If the devilsaur king fails a saving throw, it can choose to succeed instead.
>
> ***Trample.*** Whenever the devilsaur moves into an area occupied by a Medium or smaller creature, the creature must succeed on a DC 19 Strength saving throw or be knocked prone, taking 11 (2d10) bludgeoning damage.
>
> ### Actions
> ***Multiattack.*** The devilsaur king makes two attacks: one with its bite and one with its tail. It can't make both attacks against the same target.
>
> ***Bite.*** *Melee Weapon Attack:* +14 to hit, reach 10ft., one target. *Hit:* 39 (5d12 + 7) piercing damage. If the target is a Medium or smaller creature, it is grappled (escape DC 19) . Until this grapple ends, the target is restrained, and the devilsaur king can't bite another target.
>
> ***Tail.*** *Melee Weapon Attack:* +14 to hit, reach 10ft., one target. *Hit:* 25 (4d8 + 7) bludgeoning damage. If the target is a creature, it must succeed on a DC 19 Strength saving throw or be pushed up to 10 feet away from the devilsaur king and knocked prone.
>
> ***Maim.*** One grappled creature takes 59 (8d12 + 7) piercing damage. If this reduces the creature to 0 hp, the devilsaur swallows it and the grapple ends. While swallowed, the creature is blinded and restrained, it has total cover against attacks and other effects outside the devilsaur king, and it takes 21 (6d6) acid damage at the start of each of the devilsaur king's turns.
If the devil&shy;saur king takes 45 damage or more on a single turn from creatures inside it, it must succeed on a DC 15 Constitution saving throw at the end of that turn or regurgitate all swallowed creatures, which fall prone in a space within 10 feet of it. If the devilsaur king dies, a swallowed creature is no longer restrained by it and can escape from the corpse using 15 feet of movement, exiting prone.
>
> ***Terrifying Roar.***  Each creature within 60 feet of the devilsaur king that can hear him must succeed on a DC 17 Wisdom saving throw or be frightened for 1 minute. A frightened target can repeat the saving throw at the end of each of its turns, ending the frightened condition on itself on a success.
>
> ### Legendary Actions
> The devilsaur king can take 3 legendary actions, choosing from the options below. Only one legendary action option can be used at a time and only at the end of another creature's turn. The devilsaur king regains spent legendary actions at the start of his turn.
>
>**Move.** The devilsaur king moves half his speed.
> <br> **Terrifying Roar** The devilsaur king uses Terrifying Roar.
> <br> **Swallow (Costs 2 Actions).** The devilsaur king swallows <br>&nbsp;&nbsp;&nbsp; a creature it is grappling and the grapple ends. <!--https://wc5e-cr-calculator.frogvall.com/?2;15;187;14;12;75;11;75;32;75;53;0;0;0;0;0;0;;;;;3;;;;;;;;;1;1;;;;;;;;10;;;;;;-->

</div>

<div class="pageLetter">D</div>
<div class='footnote'>DINOSAURS </div>

<img src="https://www.gmbinder.com/images/ZpfPXvK.jpg" style="position:absolute; top:-49px; right:-456px; width:1380px; transform:scalex(1);">
<img src='https://www.gmbinder.com/images/M4hsHsw.png' style='position:absolute; top:60px; right:0px; width:900px' />

\pagebreakNum

<div style='margin-top:480px;'></div>

___
> ## Diemetradon
> *Large beast, unaligned*
> ___
> - **Armor Class** 13 (natural armor)
> - **Hit Points** 90 (12d10 + 24)
> - **Speed** 25 ft.
> ___
> STR | DEX | CON | INT | WIS | CHA
>|:---:|:---:|:---:|:---:|:---:|:---:|
> 14 (+2)|10 (+0)|14 (+2)|2 (-4)|12 (+1)|4 (-3)|
> ___
> - **Skills** Stealth +2
> - **Senses** passive Perception 11
> - **Languages** —
> - **Challenge** 3 (700 XP)
> ___
>
> ***Hold Breath.*** The diemetradon can hold its breath for 15 minutes.
>
> ### Actions
> ***Multiattack.*** The diemetradon makes two attacks: one with its bite and one with its claws.
>
> ***Bite.*** *Melee Weapon Attack:* +4 to hit, reach 5 ft., one target. *Hit:* 12 (3d6+2) piercing damage.
>
> ***Claw.*** *Melee Weapon Attack:* +4 to hit, reach 5 ft., one target. *Hit:* 11 (2d8+2) slashing damage.
>
> ***Silencing Howl (1/day).*** The diemetradon casts *silence*, centered on itself.<!-- https://wc5e-cr-calculator.frogvall.com/?0;13;90;4;12;23;0;0;0;0;0;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;;;;;;;;10;;;;;; -->

\columnbreak

<div style='margin-top:220px;'></div>

___
> ## Direhorn
> *Huge beast, unaligned*
> ___
> - **Armor Class** 13 (natural armor)
> - **Hit Points** 95 (10d12 + 30)
> - **Speed** 50 ft.
> ___
> STR | DEX | CON | INT | WIS | CHA
>|:---:|:---:|:---:|:---:|:---:|:---:|
> 22 (+6)|9 (-1)|17 (+3)|2 (-4)|11 (+0)|5 (-3)|
> ___
> - **Senses** passive Perception 10
> - **Languages** —
> - **Challenge** 5 (1,800 XP)
> ___
>
> ***Reflective Armor Plating.*** The direhorn has advantage on saving throws against spells and other magical effects.
>
> ***Trampling Charge.*** If the direhorn moves at least 20 feet straight toward a creature and then hits it with a gore attack on the same turn, that target must succeed on a DC 14 Strength saving throw or be knocked prone. If the target is prone, the direhorn can make one stomp attack against it as a bonus action.
>
> ### Actions
> ***Gore.*** *Melee Weapon Attack:* +9 to hit, reach 5 ft., one target. *Hit:* 24 (4d8 + 6) piercing damage.
>
> ***Stomp.*** *Melee Weapon Attack:* +9 to hit, reach 5 ft., one prone creature. *Hit:* 22 (3d10 + 6) bludgeoning damage.<!-- https://wc5e-cr-calculator.frogvall.com/?1;13;95;9;12;24;22;24;0;24;0;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;1;;;;;;;10;;;;;; -->

> ##### Variant: Incendosaur
> Found in regions of searing flames and flowing lava, an incendosaur is a distent relative to the diemetra&shy;don. An incendorsaur has the same statistics as a diemetradon, except it is immune to fire damage and replaces the diemetradon's silencing howl with the following action.
>
> ***Fire Breath (Recharge 5-6).***  The incendosaur exhales fire in a 15-foot cone. Each creature in that area must make a DC 12 Dexterity saving throw, taking 17 (5d6) fire damage on a failed save, or half as much damage on a successful one.<!-- https://wc5e-cr-calculator.frogvall.com/?0;13;90;4;12;34;0;23;0;23;0;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;;;;;;;;10;;;;;; -->

<div class="pageLetter">D</div>
<div class='footnote'>DINOSAURS </div>

<img src="https://www.gmbinder.com/images/tiU4RnD.png" class="inkblot" style="top:0px; right:-150px; width:800px">
<img src="https://www.gmbinder.com/images/C2WIUg2.png" style="position:absolute; top:0px; right:0px; width:800px;">

\pagebreakNum

<div style='margin-top:390px;'></div>

___
> ## Pterrordax
> *Large beast, unaligned*
> ___
> - **Armor Class** 14 (natural armor)
> - **Hit Points** 44 (8d10)
> - **Speed** 10 ft., fly 60 ft.
> ___
> STR | DEX | CON | INT | WIS | CHA
>|:---:|:---:|:---:|:---:|:---:|:---:|
> 10 (+0)|16 (+3)|10 (+0)|2 (-4)|13 (+1)|5 (-3)|
> ___
> - **Skills** Perception +5
> - **Senses** passive Perception 15
> - **Languages** —
> - **Challenge** 2 (450 XP)
> ___
>
> ***Flyby.*** The pterrordax doesn’t provoke an opportunity attack when it flies out of an enemy’s reach.
>
> ### Actions
> ***Multiattack.*** The pterrordax can use its Terrifying Screech. It then makes two claw attacks.
>
> ***Claw.*** *Melee Weapon Attack:* +5 to hit, reach 5 ft., one target. *Hit:* 7 (1d8 + 3) slashing damage.
>
> ***Bite.*** *Melee Weapon Attack:* +5 to hit, reach 5 ft., one target. *Hit:* 12 (2d8 + 3) piercing damage.
>
> ***Terrifying Screech.*** Each creature within 60 feet of the pterrordax that can hear it must succeed on a DC 11 Wisdom saving throw or be frightened for 1 minute. A frightened target can repeat the saving throw at the end of each of its turns, ending the frightened condition on itself on a success. If a target's saving throw is successful or the effect ends for it, the target is immune to this pterrordax's Frightful Screech for the next 24 hours.<!-- https://wc5e-cr-calculator.frogvall.com/?0;14;44;5;12;14;0;0;0;0;0;0;0;0;0;0;0;;;;;3;;;;;;;1;;;1;;;;;;;;10;;;;;; -->

\columnbreak

<div style='margin-top:271px;'></div>

___
> ## Pterrorwing
> *Huge beast, unaligned*
> ___
> - **Armor Class** 15 (natural armor)
> - **Hit Points** 85 (10d12+20)
> - **Speed** 10 ft., fly 60 ft.
> ___
> STR | DEX | CON | INT | WIS | CHA
>|:---:|:---:|:---:|:---:|:---:|:---:|
> 13 (+1)|17 (+3)|14 (+2)|2 (-4)|14 (+2)|5 (-3)|
> ___
> - **Skills** Perception +8
> - **Senses** passive Perception 18
> - **Languages** —
> - **Challenge** 5 (1800 XP)
> ___
>
> ***Flyby.*** The pterrorwing doesn’t provoke an opportunity attack when it flies out of an enemy’s reach.
>
> ### Actions
> ***Multiattack.*** The pterrorwing can use its Terrifying Screech. It then makes three attacks: one with its bite and two with its claws.
>
> ***Claw.*** *Melee Weapon Attack:* +6 to hit, reach 5 ft., one target. *Hit:* 7 (1d8 + 3) slashing damage.
>
> ***Bite.*** *Melee Weapon Attack:* +6 to hit, reach 5 ft., one target. *Hit:* 12 (2d8 + 3) piercing damage.
>
> ***Terrifying Screech.*** Each creature within 60 feet of the pterrorwing that can hear it must succeed on a DC 15 Wisdom saving throw or be frightened for 1 minute. A frightened target can repeat the saving throw at the end of each of its turns, ending the frightened condition on itself on a success. If a target's saving throw is successful or the effect ends for it, the target is immune to this pterrorwing's Frightful Screech for the next 24 hours.
>
> ***Skycall (Recharge 5-6).*** The pterrorwing screams and a thunderous force sweeps out from it in a 15 foot cone. Each creature in that area must make a DC 15 Constitution saving throw, taking 33 (6d10) thunder damage on a failed save and is pushed 15 feet away from it. On a successful save, the creature takes half as much damage and isn't pushed.<!-- https://wc5e-cr-calculator.frogvall.com/?1;15;85;6;12;66;0;26;0;26;0;0;0;0;0;0;0;;;;;3;;;;;;;1;;;1;;;;;;;;10;;;;;; -->

<img src="https://www.gmbinder.com/images/0hVRLNf.png" class="inkblot" style="top:-100px; right:80px; width:800px; transform:rotate(120deg)">
<img src='https://www.gmbinder.com/images/LHF6snZ.png' style='position:absolute; top:27px; right:50px; width:720px' />

<div class="pageLetter">D</div>
<div class='footnote'>DINOSAURS </div>

\pagebreakNum

<div style='margin-top:84px;'></div>

> ##### Variant: Ravagers and Falcosaurs
> Some raptors are referred to as ravagers. A **raptor ravager** has the statistics of a raptor, a challenge rating of 2 (450 XP) and the following traits:
>
> <br>&nbsp;&nbsp;&nbsp; **Rampage.** When the raptor reduces a creature to <br>&nbsp;&nbsp;&nbsp; 0 hit points with a melee attack on its turn, the <br>&nbsp;&nbsp;&nbsp; raptor can take a bonus action to move up to half <br>&nbsp;&nbsp;&nbsp; its speed and make a bite attack.<!-- https://wc5e-cr-calculator.frogvall.com/?0;13;27;5;12;14;0;0;0;0;0;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;;;1;;;1;;10;;;;;; -->
>
> <br> Falcosaurs are invasive predatory dinosaurs found on the coastlines of the Broken Isles, that resemble fea&shy;thered raptors with huge beaks for maws. A **falcosaur raptor** uses the statistics of a raptor and a raptor matriarch, and has the following trait:
>
> <br>&nbsp;&nbsp;&nbsp; ***Natural Camouflage.*** The falcosaur has advantage <br>&nbsp;&nbsp;&nbsp; on Dexterity (Stealth) checks made to hide.

___
> ## Raptor
>*Medium beast, unaligned*
> ___
> - **Armor Class** 13 (Natural Armor)
> - **Hit Points** 27 (5d8 + 5)
> - **Speed** 50 ft
> ___
>|STR|DEX|CON|INT|WIS|CHA|
>|:---:|:---:|:---:|:---:|:---:|:---:|
>|12 (+1)|16 (+3)|12 (+1)|3 (-4)|14 (+2)|6 (-2)|
> ___
> - **Skills** Perception +4, Stealth +4
> - **Senses** passive Perception 14
> - **Languages** —
> - **Challenge** 1 (200 XP)
> ___
> ***Keen Hearing and Smell.*** The raptor has advantage on Wisdom (Perception) checks that rely on hearing or smell.
>
> ***Pack Tactics.*** The raptor has advantage on attack rolls against a creature if at least one of the raptor's allies is within 5 feet of the creature and the ally isn't incapacitated.
>
> ***Pounce***. If the raptor moves at least 20 ft. straight toward a creature and then hits it with a claw or bite attack on the same turn, that target must succeed on a DC 13 Strength saving throw or be knocked prone.
>
> ### Actions
> ***Multiattack.*** The raptor makes two attacks: one with its bite and one with its claws.
>
> ***Bite***. Melee Weapon Attack: +5 to hit, reach 5 ft., one creature. Hit: 6 (1d6+3) piercing damage.
>
> ***Claws***. Melee Weapon Attack: +5 to hit, reach 5 ft., one creature. Hit: 8 (1d8+3) slashing damage.<!-- https://wc5e-cr-calculator.frogvall.com/?0;13;27;5;12;14;0;0;0;0;0;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;;;1;;;;;10;;;;;; -->

\columnbreak

<div style='margin-top:314px;'></div>

___
> ## Raptor Matriarch
>*Medium beast, unaligned*
> ___
> - **Armor Class** 13 (Natural Armor)
> - **Hit Points** 65 (10d8 + 20)
> - **Speed** 50 ft
> ___
>|STR|DEX|CON|INT|WIS|CHA|
>|:---:|:---:|:---:|:---:|:---:|:---:|
>|12 (+1)|17 (+3)|14 (+2)|8 (-1)|14 (+2)|12 (+1)|
> ___
> - **Skills** Perception +4, Stealth +5, Intimidation +3
> - **Senses** passive Perception 14
> - **Languages** —
> - **Challenge** 3 (700 XP)
> ___
> ***Keen Hearing and Smell.*** The raptor has advantage on Wisdom (Perception) checks that rely on hearing or smell.
>
> ***Pack Tactics.*** The raptor has advantage on attack rolls against a creature if at least one of the raptor's allies is within 5 feet of the creature and the ally isn't incapacitated.
>
> ***Pounce***. If the raptor moves at least 20 ft. straight toward a creature and then hits it with a claw or bite attack on the same turn, that target must succeed on a DC 13 Strength saving throw or be knocked prone.
>
> ### Actions
> ***Multiattack.*** The raptor makes two attacks: one with its bite and one with its claws.
>
> ***Bite***. Melee Weapon Attack: +5 to hit, reach 5 ft., one creature. Hit: 10 (2d6+3) piercing damage.
>
> ***Claws***. Melee Weapon Attack: +5 to hit, reach 5 ft., one creature. Hit: 12 (2d8+3) slashing damage.
>
> ***Matron's Call (1/Day).*** The raptor utters a series of guttural noises and cries. Other raptors within 30 ft. who hear the call, can use their reaction to make an opportunity attack against a creature within 5 ft. of them.<!-- https://wc5e-cr-calculator.frogvall.com/?0;13;65;5;12;22;0;0;0;0;0;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;;;1;;;;;10;;;;;; -->

<div class="pageLetter">D</div>
<div class='footnote'>DINOSAURS </div>

<img src="https://www.gmbinder.com/images/KcRAZwq.png" class="inkblot" style="top:-300px; right:0px; width:800px; transform:rotate(40deg)">
<img src='https://www.gmbinder.com/images/ZlkfRr5.png' style='position:absolute; top:-40px; right:-230px; width:900px; transform:scalex(-1)' />

\pagebreakNum

<div style='margin-top:380px;'></div>

___
> ## Sabertusk
> *Large beast, unaligned*
> ___
> - **Armor Class** 14 (natural armor)
> - **Hit Points** 65 (10d10 + 10)
> - **Speed** 40 ft.
> ___
> STR | DEX | CON | INT | WIS | CHA
>|:---:|:---:|:---:|:---:|:---:|:---:|
> 11 (+0)|18 (+4)|12 (+1)|2 (-4)|15 (+2)|9 (-1)|
> ___
> - **Skills** Perception +6, Stealth +6, Survival +4
> - **Senses** passive Perception 16
> - **Languages** —
> - **Challenge** 3 (700 XP)
> ___
>
> ***Keen Smell.*** The sabertusk has advantage on Wisdom (Perception) checks that rely on smell.
>
> ***Pounce.*** If the sabertusk moves at least 20 feet straight toward a creature and then hits it with a claw attack on the same turn, that target must succeed on a DC 14 Strength saving throw or be knocked prone. If the target is prone, the sabertusk can make one bite attack against it as a bonus action.
>
> ***Tendon Rip.*** If the sabertusk hits the same creature with two claw attacks in the same turn, the creature takes another 7 (2d6) slashing damage and its speed is halved until the end of its next turn.
>
> ### Actions
> ***Multiattack.*** The sabertusk makes two claw attacks.
>
> ***Bite.*** *Melee Weapon Attack:* +6 to hit, reach 5 ft., one target. *Hit:* 13 (2d8+4) piercing damage.
>
> ***Claw.*** *Melee Weapon Attack:* +6 to hit, reach 5 ft., one target. *Hit:* 7 (1d6+4) slashing damage.<!-- https://wc5e-cr-calculator.frogvall.com/?0;14;65;6;12;14;20;14;7;14;7;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;;;;;;;;10;;;;;; -->

\columnbreak

<div style='margin-top:481px;'></div>

___
> ## Saurid
> *Tiny beast, unaligned*
> ___
> - **Armor Class** 11 (natural armor)
> - **Hit Points** 12 (5d4)
> - **Speed** 25 ft.
> ___
> STR | DEX | CON | INT | WIS | CHA
>|:---:|:---:|:---:|:---:|:---:|:---:|
> 7 (-2)|13 (+1)|11 (+0)|2 (-4)|10 (+0)|4 (-3)|
> ___
> - **Senses** passive Perception 10
> - **Languages** —
> - **Challenge** 1/2 (100 XP)
> ___
>
> ***Keen Smell.*** The saurid has advantage on Wisdom (Perception) checks that rely on smell.
>
> ***Pack Tactics.*** The saurid has advantage on an attack roll against a creature if at least one of the saurid's allies is within 5 feet of the creature and the ally isn't incapacitated.
>
> ### Actions
> ***Attack.*** *Melee Weapon Attack:* +3 to hit, reach 5 ft., one target. *Hit:* 3 (1d4+1) piercing damage, and the target must succeed on a DC 11 Constitution saving throw or take 7 (3d4) poison damage and be poisoned for 1 minute. The target can repeat the saving throw at the end of each of its turns, ending the poison on itself on a success.<!-- https://wc5e-cr-calculator.frogvall.com/?0;11;12;3;12;10;0;0;0;0;0;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;;;1;;;;;10;;;;;; -->

<div class="pageLetter">D</div>
<div class='footnote'>DINOSAURS </div>

<img src="https://www.gmbinder.com/images/0hVRLNf.png" class="inkblot" style="top:-100px; right:110px; width:730px; transform:rotate(479deg);">
<img src="https://www.gmbinder.com/images/x2uBrWh.png" style="position:absolute; top:50px; right:150px; width:600px;">

\pagebreakNum

___
> ## Threshadon
>*Huge beast, unaligned*
> ___
> - **Armor Class** 14 (natural armor)
> - **Hit Points** 60 (7d10 + 22)
> - **Speed** 20 ft., swim 40 ft.
>___
>|STR|DEX|CON|INT|WIS|CHA|
>|:---:|:---:|:---:|:---:|:---:|:---:|
>|18 (+4)|15 (+2)|14 (+2)|2 (-4)|12 (+1)|5 (-3)|
>___
> - **Skills** Perception +3, Stealth +4
> - **Senses** passive Perception 13
> - **Languages** —
> - **Challenge** 3 (700 XP)
> ___
> ***Hold breath.*** The threshadon can hold its breath for 30 minutes.
>
> ***Keen Hearing.*** The threshadon has advantage on Wisdom (Perception) checks that rely on hearing.
>
> ***Relentless (Recharges after a Short or Long Rest).*** <br> If the threshadon takes 12 points of damage or less that would reduce it to 0 hit points, it is reduced to 1 hit point instead.
>
> ### Actions
> ***Multiattack.*** The threshadon makes two bite attacks. 
>
> ***Bite.*** *Melee Weapon Attack*: +6 to hit, reach 10 ft., one target. Hit: 14 (3d6 + 4) piercing damage.<!-- https://wc5e-cr-calculator.frogvall.com/?0;14;60;6;12;28;0;0;0;0;0;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;;;;;;;;10;1;;;;; -->

\columnbreak

___
> ## Stegodon
>*Huge beast, unaligned*
> ___
> - **Armor Class** 14 (natural armor)
> - **Hit Points** 95 (10d12 + 30)
> - **Speed** 40 ft.
>___
>|STR|DEX|CON|INT|WIS|CHA|
>|:---:|:---:|:---:|:---:|:---:|:---:|
>|21 (+5)|9 (-1)|17 (+3)|4 (-3)|11 (+0)|6 (-2)|
>___
> - **Senses** passive Perception 10
> - **Languages** —
> - **Challenge** 4 (1,100 XP)
> ___
> ***Trampling Charge.*** If the stegodon moves at least 20 feet straight towards a creature and then hits it with a gore attack on the same turn, that target must succeed on a DC 13 Strength saving throw or be knocked prone. If the target is prone, the stegadon can make one stomp attack against it as a bonus action.
>
> ### Actions
> ***Gore.*** *Melee Attack Weapon:* +7 to hit, reach 5 ft., one target. *Hit:* 18 (3d8 + 5) piercing damage.
>
> ***Stomp.*** *Melee Attack Weapon:* +7 to hit, reach 5 ft., one target. *Hit:* 21 (3d10 + 5) bludgeoning damage.
>
> ***Impale***. *Melee Weapon Attack:* +7 to hit, reach 10 ft., one creature. *Hit:* 23 (4d8 + 5) piercing damage. If the target is a Medium or smaller creature, it is grappled (escape DC 13). Until this grapple ends, the target is restrained, and the stegadon can't use its impale on another target.<!-- https://wc5e-cr-calculator.frogvall.com/?0;14;95;7;12;18;21;23;0;21;0;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;;;;;;;;10;;;;;; -->

<div class="pageLetter">D</div>
<div class='footnote'>DINOSAURS </div>

<img src='https://www.gmbinder.com/images/qJf7wgU.jpg' style='position:absolute; top:450px; right:-300px; width:1200px' />
<img src='https://www.gmbinder.com/images/MVDaLa2.png' style='position:absolute; top:-200px; right:0px; width:800px; transform:scalex(-1)' />


\pagebreakNum