<style>.phb{width : 210mm;height : 296.8mm;} .phb:after {content: "";} </style>
<style>.phb hr+section blockquote { padding-left: 0px; padding-right: 0px; }</style>
<style>.phb blockquote { padding-left: 0px; padding-right: 0px; }</style>
<style> .phb blockquote { margin-top: 1em; } </style>


<style>

/* TABLES AND BLOCKS */

  /* Clear internal padding and add gap above for green note blocks*/
  .phb blockquote {
    padding-left: 0px;
    padding-right: 0px;
  }
  .phb blockquote { margin-top: 1em;
  }
  
  /* Use black tones for statblock backgrounds */
  .phb blockquote {
    box-shadow: 1px 4px 14px rgba(0,0,0,0.42);
  }
  

/* APPENDIX STYLES */

  /* Avoid upscaling first letter on an appendix page */
  .phb:nth-of-type(n+0):nth-of-type(-n+100) h1+p::first-letter {
    font-family: BookSanity;
    font-size: .317cm;
    text-rendering: optimizeLegibility;
    float: initial;
  }
  
  /* For creature statblocks within range (start and end must be specified),
  don't show a background. Used for the appendix creatures */
  .phb:nth-of-type(n+0):nth-of-type(-n+100) hr+section blockquote {
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

/* FOOTER STYLES  */

  .phb .pageNumber { color: #7e735c; z-index:1000; }
  .phb .footnote { color: #7e735c; }
  
  .phb:nth-child(odd):after {
    content: '';
    height: 125px;
    background-image: url(https://www.gmbinder.com/images/PB8On0U.png), url('https://gmbinder.com/images/YWardeu.png');
    background-size: 120px 120px, 816px 55px;
    background-repeat: no-repeat, no-repeat;
    background-position: bottom right -10px, bottom;
  }

  /* Reversed for alternating pages */
  .phb:nth-child(even):after {
    content: '';
    height: 125px;
    background-image: url(https://www.gmbinder.com/images/PB8On0U.png), url('https://gmbinder.com/images/YWardeu.png');
    background-size: 120px 120px, 816px 55px;
    background-repeat: no-repeat, no-repeat;
    background-position: bottom right -10px, bottom;
    -webkit-transform: scaleX(-1);
    transform: scaleX(-1);
  }    


/* Monster Manual alphabetical chapter letters */

.mml-a {background-image: url(https://gmbinder.com/images/fVVv93s.png);}
.mml-b {background-image: url(https://gmbinder.com/images/21X6N0B.png);}
.mml-c {background-image: url(https://gmbinder.com/images/MvnpOWF.png);}
.mml-d {background-image: url(https://gmbinder.com/images/AFbLU4P.png);}
.mml-e {background-image: url(https://gmbinder.com/images/28NVNf9.png);}
.mml-f {background-image: url(https://gmbinder.com/images/Oyrhmqy.png);}
.mml-g {background-image: url(https://gmbinder.com/images/fRyiQn4.png);}
.mml-h {background-image: url(https://gmbinder.com/images/N8NamlT.png);}
.mml-i {background-image: url(https://gmbinder.com/images/xWI93aa.png);}
.mml-j {background-image: url(https://gmbinder.com/images/GgIzsun.png);}
.mml-k {background-image: url(https://gmbinder.com/images/OcObsWl.png);}
.mml-l {background-image: url(https://gmbinder.com/images/B7AUyR6.png);}
.mml-m {background-image: url(https://gmbinder.com/images/q4wXoxt.png);}
.mml-n {background-image: url(https://gmbinder.com/images/OJtC4w9.png);}
.mml-o {background-image: url(https://gmbinder.com/images/adeRr5d.png);}
.mml-p {background-image: url(https://gmbinder.com/images/EEhcrSR.png);}
.mml-q {background-image: url(https://gmbinder.com/images/O1AhfzL.png);}
.mml-r {background-image: url(https://gmbinder.com/images/w66eIuZ.png);}
.mml-s {background-image: url(https://gmbinder.com/images/YEoe0PP.png);}
.mml-t {background-image: url(https://gmbinder.com/images/7Bk9D35.png);}
.mml-u {background-image: url(https://gmbinder.com/images/uVJZYUg.png);}
.mml-v {background-image: url(https://gmbinder.com/images/gKjngey.png);}
.mml-w {background-image: url(https://gmbinder.com/images/14WWpsC.png);}
.mml-x {background-image: url(https://gmbinder.com/images/ojIYjh0.png);}
.mml-y {background-image: url(https://gmbinder.com/images/Gi1ePwY.png);}
.mml-z {background-image: url(https://gmbinder.com/images/0ZTFNVs.png);}

/* letter at bottom of page */

  .pageLetter {
    font-family:;
    position:absolute;
    right:25px;
    bottom:87.5px;
    color:#673e1c;
    z-index:1000;
    font-size:135%;
  }

  .phb:nth-child(even) .pageLetter {
    left:25px;
  }

/* BACK PAGE STYLES */

  /* Remove footer from back page, replace pX with last page num */
  .phb#p19:after { display:none; }

  .phb .back-cover-content {
    padding-left: 4px;
    padding-right: 16px;
  }
  .phb .back-cover-right {
      padding-left: 40px;
  }
  .phb .back-cover-image {
    height: 1136px;
    left: -20px;
    top: -10px;
    width: 475px;
    background-size: 475px 1136px;
  }
  .phb .back-cover-diamond {
    display: block;
    position: initial;
    left: initial;
    top: initial;
    margin: auto;
    margin-bottom: 35px;
    box-sizing: border-box;
    background-repeat: no-repeat;
  }
 .phb .back-cover-logo-container {
    position: absolute;
    bottom: 30px;
    left: 64px;
    width: 314px;
 }
 .phb .back-cover-logo,
 .phb .back-cover-logo-link {
     position: initial;
     margin: auto;
     margin-bottom: 8px;
     left: initial;
     bottom: initial;
     right: initial;
     background-repeat: no-repeat;
 }
 
</style>

# Noth the Plaguebringer
*"Behold, Noth the Plaguebringer. Responsible for the creation of the process that distills the souls of the living and places them within the cold cage of undeath, Noth was observed to be refining this process even now."*
<div style="text-align: right">- Commander Eligor Dawnbringer</div>

\columnbreak

Noth the Plaguebringer was once a reputable mage of Dalaran, who heard the call of the Lich King in much the same way Kel'Thuzad did. Also driven by power, he accepted the summons to serve the needs of the Scourge with his skills in necromancy and curse-weaving. However, when Noth saw that the Third War was taking numerous innocent lives, he began second-guessing his decision to join Kel'Thuzad. Kel'Thuzad swiftly dealt with Noth's growing compassion by freezing the living heart in Noth's chest.

<div class='statblock-bottom-wide'>

___
___
> ## Noth the Plaguebringer <!-- https://wc5e-cr-calculator.frogvall.com/?3;15;360;12;21;49;59;98;118;98;118;0;0;0;0;0;0;1;;;;3;;;;;;;;;1;3;1;;;;;;;10;;;;;;;2;2;1;3;1;0;1; -->
> *Medium undead, neutral evil*
> ___
> - **Armor Class** 15 (natural armor)
> - **Hit Points** 300 (40d8 + 120)
> - **Speed** 30 ft.
> ___
> STR | DEX | CON | INT | WIS | CHA
>|:---:|:---:|:---:|:---:|:---:|:---:|
> 9 (-1)|17 (+3)|16 (+3)|23 (+6)|20 (+5)|17 (+3)|
> ___
> - **Saving Throws** Con +9, Int +12, Wis +11, Cha +9
> - **Skills** Arcana +12, Deception +9, History +12, Intimidation +9
> - **Damage Resistances** bludgeoning, piercing, and slashing from nonmagical attacks that aren't adamantine
> - **Damage Immunities** necrotic, poison;
> - **Condition Immunities** charmed, exhaustion, frightened, poisoned
> - **Senses** darkvision 60 ft., passive Perception 15
> - **Languages** common
> - **Challenge** 22 (41,000 XP)
> ___
>
> ***Legendary Resistance (3/Day).*** If Noth fails a saving throw, he can choose to succeed instead.
> 
> ***Magic Resistance.*** Noth has advantage on saving throws against spells and other magical effects.
>
> ***Wrath of the Plaguebringer.*** On each of his turns in combat, Noth can use a bonus action to force every creature cursed by curse of the plaguebringer to make a DC 21 Constitution saving throw, taking 33 (6d10) necrotic damage on a failed save, and half as much on a successful save.
>
> ### Actions
> ***Blink (Recharge 4-6).*** *Cripple is recharged. Noth teleports up to 30 feet to an unoccupied space that he can see.
>
> ***Cripple (Recharge 4-6).*** *Blink* is recharged. Each non-undead, non-construct creature within 30 feet of Noth must make a DC 21 Constitution saving throw, taking 13 (3d8) necrotic damage and have their speed reduced to 10 feet, have disadvantage on attack rolls and if they have the *Extra attack* feature they can't benefit from it until the start of Noth's next turn on a failed save. On a successful save the creature takes half as much damage and suffers none of the other effects. 
>
> ***Curse of the Plaguebringer.*** One non-undead, non-construct creature that Noth can see must make a Charisma DC 21 saving throw or be cursed with the curse of the plaguebringer. While cursed the creature has disadvantage on Charisma saves and takes 16 (3d10) necrotic damage at the start of its turn. At the end of the creature's turn, it can repeat the saving throw, ending the curse on a success. Casting *remove curse*, *greater restoration*, or a similar spell on the target also ends the curse.
>
> ***Inject Plague.*** *Melee Weapon Attack:* +12 to hit, reach 5 ft., one creature. Hit: 28 (4d10 + 6) necrotic damage.
>
> ### Legendary Actions
> Noth can take 3 legendary actions, choosing from the options below. Only one legendary action option can be used at a time and only at the end of another creature’s turn. Noth regains spent legendary actions at the start of its turn.
>
> ***Blink.*** Noth uses Blink.
>
> ***Cripple.*** Noth uses Cripple.
>
> ***Summon Plagued Warrior.*** A *plagued warrior* is summoned at any unoccupied space within 30 feet of Noth.
>
> ***Wrath of the Plaguebringer. (Costs 2 Actions)*** Noth uses Wrath of the Plaguebringer.
> 
> ***Phase Shift (Costs 3 Actions).*** Two *plagued guardians* and two *plagued champions* are summoned within 30 feet of Noth, rolling initiative as normal. Noth then disappears to another plane. When all the above undead are killed, he reappears in the same space he disappeared in if unoccupied or in the closest unoccupied space if not. After reappearing, Noth have to take his turn twice before he can use *Phase Shift* again.
</div>

<img src='https://www.gmbinder.com/images/hNSunqw.jpg' style='position:absolute; top:780px; right:0px; width:400px; transform:scalex(-1)' />
<img src="https://www.gmbinder.com/images/qKrtKxo.png" style="position:absolute; top:0px; right:-50px; width:950px; transform:scaley(-1)">
<img src="https://www.gmbinder.com/images/TYBvp5o.png" style="position:absolute; top:230px; right:-100px; width:900px; transform:scaley(-1)">


\pagebreak

### Noth the Plaguebringer's Lair
From within his champers in the Plague Quarter of Naxxramas, Noth is an even bigger threat as he has access to an almost infinite stream of dead bodies to resurrect.

#### Lair Actions
On initiative count 20 (losing initiative ties), two *plagued warriors* are summoned at any unoccupied spaces bordering the edge of the room, rolling initiative as normal.
<br/><br/>
&nbsp;&nbsp;&nbsp;&nbsp;***Note:*** The CR (and XP) for Noth already assumes there will be *plagued warriors*, *plagued guardians* and *plagued champions* summoned. DMs should not award XP for those summoned by Noth's abilities. Warriors summoned by the Lair actions however is not included in the CR calculation. If you use Noth's Lair, award XP for the *plagued warriors* summoned by the lair. Also note that the fight will be more dangerous within Noth's Lair.

***Design notes:*** I tried to make this fight as close to the original source as possible, however:

* Teleporting to a balcony within the same room as the player's will not stop the players from going after Noth, like it does in WoW. Hence the *Phase Shift* instead. If you want the effect of the balcony, have an avatar of Noth show up on the balcony to taunt the player's or something similar.
* *Inject Plague* was added to give Noth something to do in the odd occurance that everyone is already cursed. It was an ability found on other plaguebringers in WoW.
* Action economy and damage throughput in 5e does not make swarms of undead very viable (they would have to be so weak so that any character with a meaningful AoE would be able to wipe them even on a successful save). I instead focused on a fewer number of semi powerful foes.

___
> ## Plagued Warrior <!-- https://wc5e-cr-calculator.frogvall.com/?0;13;45;8;12;24;0;0;0;0;0;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;;;;;;;;10;;;;;;;2;2;1;3;1;0;1; -->
>*Medium undead, neutral evil*
> ___
> - **Armor Class** 13 (natural armor)
> - **Hit Points** 45 (7d8 + 14)
> - **Speed** 30 ft.
>___
>|STR|DEX|CON|INT|WIS|CHA|
>|:---:|:---:|:---:|:---:|:---:|:---:|
>|23 (+6)|11 (+0)|14 (+2)|3 (-4)|6 (-2)|5 (-3)| 
>___
> - **Damage Immunities** poison
> - **Condition Immunities** poisoned
> - **Senses** darkvision 60 ft., passive Perception 8
> - **Languages** understands the languages it knew in life but can't speak
> - **Challenge** 3 (700 XP)
> ___
>
> ### Actions
> ***Multiattack.*** The warrior makes two greatsword attacks.
>
> ***Cleave.*** *Melee Weapon Attack:* +8 to hit, reach 5ft., up to three targets. *Hit:* 12 (2d6 + 5) slashing damage.
>
> ***Greatsword.*** *Melee Weapon Attack:* +8 to hit, reach 5 ft., one target. *Hit:* 12 (2d6 + 5) slashing damage.

\columnbreak

___
> ## Plagued Guardian <!-- https://wc5e-cr-calculator.frogvall.com/?0;13;52;4;18;18;18;0;0;0;0;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;;;;;;;;10;;;;;;;2;2;1;3;1;0;1; -->
>*Medium undead, neutral evil*
> ___
> - **Armor Class** 13 (natural armor)
> - **Hit Points** 52 (8d8 + 16)
> - **Speed** 30 ft.
>___
>|STR|DEX|CON|INT|WIS|CHA|
>|:---:|:---:|:---:|:---:|:---:|:---:|
>|8 (-1)|11 (+0)|14 (+2)|19 (+4)|12 (+1)|5 (-3)|
>___
> - **Damage Immunities** poison
> - **Condition Immunities** poisoned
> - **Senses** darkvision 60 ft., passive Perception 11
> - **Languages** understands the languages it knew in life but can't speak
> - **Challenge** 4 (1100 XP)
> ___
>
> ### Actions
> ***Arcane Explosion.*** Each non-undead, non-construct creature within 15 feet of the guardian have to make a DC 18 Dexterity saving throw or take 18 (4d8) force damage.
> 
> ### Reactions
> ***Blink.*** When the guardian takes damage it can teleport 30 feet to an unoccupied space that it can see.

___
> ## Plagued Champion <!-- https://wc5e-cr-calculator.frogvall.com/?1;16;58;10;18;27;27;0;0;0;0;0;0;0;0;0;0;;;;;3;;;;;;;;;;1;;;;;;;;10;;;;;;;2;2;1;3;1;0;1; -->
>*Medium undead, neutral evil*
> ___
> - **Armor Class** 16 (plate armor)
> - **Hit Points** 58 (9d8 + 18)
> - **Speed** 30 ft.
>___
>|STR|DEX|CON|INT|WIS|CHA|
>|:---:|:---:|:---:|:---:|:---:|:---:|
>|25 (+7)|11 (+0)|14 (+2)|3 (-4)|6 (-2)|19 (+4)|
>___
> - **Damage Immunities** poison
> - **Condition Immunities** poisoned
> - **Senses** darkvision 60 ft., passive Perception 8
> - **Languages** understands the languages it knew in life but can't speak
> - **Challenge** 6 (2300 XP)
> ___
>
> ### Actions
> ***Multiattack.*** The champion makes two melee attacks.
>
> ***Mortal Strike.*** *Melee Weapon Attack:* +10 to hit, reach 5ft., one target. *Hit:* 11 (1d8 + 7) slashing and 13 (3d8) necrotic damage and a non-undead, non-construct target cannot regain hit points until the start of the champion's next turn.
>
> ***Shadow Shock.*** Each creature within 15 feet of the champion have to make a DC 18 Dexterity saving throw or take 27 (6d8) necrotic damage. 