# Armor Alley: Web Prototype

Copyright (c) 2013, Scott Schiller
http://www.schillmania.com/armor-alley/
http://www.schillmania.com/content/entries/2013/armor-alley-web-prototype/
http://github.com/scottschiller/ArmorAlley/

Code provided under the Attribution-NonCommercial 3.0 Unported (CC BY-NC 3.0) License:
http://creativecommons.org/licenses/by-nc/3.0/

-----

## Changelog / Revision History

### V1.51.20181124

**Performance tweaks**

 • More motion / animation is now on the GPU via `transform`, vs. `style.left` / `style.top`.

 • Main animation loop calls `requestAnimationFrame()` first, before anything else (like VSYNC.)

 • Drop legacy SM2 flash options.

 • Turret scan is now driven by CSS animation vs. JS setting an angle transform every frame.

**Sound**

 • New base explosion, tweaked other explosion sound effects.

 • New "heavy mechanics" bunker chain (repair) sound.

### V1.5.20180201

**Big feature updates!**

 • Game "mostly" now works on mobile devices. Touch-based events for helicopter control, UI for helicopter weapons and inventory / ordering. Tested on iPhone X. Others should work reasonably-well. Hopefully.

 • Inventory order queueing! 🎉 (Finally.) e.g., 3 tanks in a row. Queueing deducts funds immediately. No added UI or cancel ability (yet.)

 • Battlefield view is now bigger on screen. Stats UI is dead, long live stats.
  
 • Performance improvements. tl;dr: JavaScript tweaks, putting most all sprites onto the GPU. Replaced most common animated .GIF backgrounds with 3d-transform, GPU-accelerated CSS animation-driven sprites. 😅

**Sound**
 
 • No sound for any Safari (desktop or mobile) for now, including version 11.0. Multiple sounds kill performance on desktop, and "auto-play" is effectively blocked on mobile. https://bugs.webkit.org/show_bug.cgi?id=116145

 • New + improved helicopter machine gun sounds. 9 different samples, played at random.

 • New sound effects: "bomb hatch" (helicopter bomb release), tank gunfire, bunker chain/balloon repair, helicopter gunfire hit.

 • "Medals clanking" sound for bunker chain/balloon repair. (BY-NC 3.0.) https://freesound.org/people/Gareth_H/sounds/365799/

 • New tank gunfire sound: "Tank Fire Mixed.wav" by Cyberkineticfilms/freesound.org (CC0, "No Rights Reserved". 🙇)

 • Hat tip: "Bolo" "tank self hit" sound effect, Copyright (C) Steuart Cheshire 1993. My favourite Mac game of all time. ❤️

**UX / UI**
  
 • "Radar jammed" TV static-like overlay with transform sprite.

 • Parachute infantry swing in the air thanks to CSS animations, and move more smoothly when the wind picks up.

 • Jam radar all the time when an enemy van is within range on hard + extreme game types. (previously, jamming could switch on/off at random intervals.)

 • Slightly faster helicopter bombing rate - more responsive.
  
 • Chain refactor. Use fixed height, animate via transform, fall with gravity when balloon and/or bunker are lost.

 • Balloons are yellow-ish on radar, and now transform-rotated to elliptical shapes. Bunkers / base color and border tweaks, friendly vs. enemy now look different.

 • Inventory and helicopter ammo, etc., become greyed out when unaffordable / unavailable.

 • Target / "tracking" animation on Smart Missile targets.

 • Smart Missiles can now re-target on the next frame after the original target dies. If a new target can not be immediately acquired, the Smart Missile dies as previously.

 • Radar items, clouds and some other sprites move more smoothly simply by dropping `parseInt()`.

 • "C" / rubber chicken use causes UI to switch to rubber chicken mode.

 • Possible bugfix: If paused and enemy order timer fires, re-start timer. This probably fixes enemy inventory building sometimes breaking.


**Miscellany**

 • Note re: Firefox `will-change` memory consumption warning that might show in console.

 • URL feature flags: `noTranslate3d` and `noRadarGPU`. `frameRate=[60|*]` for testing of `requestAnimationFrame()` timing. camelCase others. Let Opera (now webkit-based) have transforms.

 • +`makeTransformSprite()`, a sort of sub-sprite for CSS transform-based animations (GPU-accelerated animated .GIF alternatives.)

 • `z-index: -1` can be harmful for performance / compositing.

 • iPhone X notch handling based on orientation and whatnot.

-----

## License

(ISC license applies to original game images and related assets, used with permission)

Armor Alley (original MS-DOS version)
http://en.wikipedia.org/wiki/Armor_alley

Copyright (c) 1990, Information Access Technologies

Permission to use, copy, modify, and/or distribute this software for any purpose
with or without fee is hereby granted, provided that the above copyright notice
and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH
REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND
FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT,
INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS
OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER
TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE
OF THIS SOFTWARE.

-----

## Acknowledgements and Credits

Many thanks are due to the original game author for granting permission
to use the Armor Alley images and related assets under an ISC license.
http://opensource.org/licenses/ISC

As the original sound effects could not be re-licensed, modern
(and higher-fidelity) sound effects were found on http://freesound.org

Thanks go to numerous individuals for making their work available.
The majority of these sounds have been published under a Creative Commons
Attribution license, or other as specified. Details at each link.

### Sounds

`01587 helicopter.wav` by Robinhood76
http://freesound.org/people/Robinhood76/sounds/94867/

`Click` by lebcraftlp
http://freesound.org/people/lebcraftlp/sounds/192279/

`Cloth Flaps` by Sauron974
http://freesound.org/people/Sauron974/sounds/188733/

`DarkDetonation01.wav` by M-RED
http://freesound.org/people/M-RED/sounds/183870/

`Debris Sifting Dry.aif` by kantouth
http://freesound.org/people/kantouth/sounds/115113/

`explosion.mp3` by sarge4267
http://freesound.org/people/sarge4267/sounds/102719/

`explosion3.wav` by sarge4267
http://freesound.org/people/sarge4267/sounds/102733/

`explosion 4.aif` by harpoyume
http://freesound.org/people/harpoyume/sounds/86032/

`Gunshot 1.wav` by Adam_N
http://freesound.org/people/Adam_N/sounds/164667/

`GunShot.03.wav` by stintx
http://freesound.org/people/stintx/sounds/107620/

`Warfare_gunshots_machine_gun_burst_001.wav` by soundscalpel.com
http://freesound.org/people/soundscalpel.com/sounds/110622/

`oddworld_bomb.wav` by Oddworld
http://freesound.org/people/Oddworld/sounds/75330/

`D6.wav` by RealRhodesSounds
http://freesound.org/people/RealRhodesSounds/sounds/4194/

`snapping-chain` by CosmicEmbers
http://freesound.org/people/CosmicEmbers/sounds/161650/

`Stapler_Hands_05.wav` by Simon Lacelle
http://freesound.org/people/Simon_Lacelle/sounds/67352/

`static.wav` by g_lowing
http://freesound.org/people/g_lowing/sounds/84432/

`vhs hum` by jocobzeier
http://freesound.org/people/jacobzeier/sounds/166178/

`Metal Click Sound` by mkoenig
http://freesound.org/people/mkoenig/sounds/81175/

`impact_water_splash_bomb_throw_flesh_01.wav` by m_O_m
http://freesound.org/people/m_O_m/sounds/108758/

`Faulty Flourescent Light Start & Hum.wav` by EverydaySounds
http://freesound.org/people/EverydaySounds/sounds/125064/

`Wilhem Scream Sample (1951)`
http://archive.org/details/WilhelmScreamSample

`imppact wrench bounce.wav` by andrewgnau2
http://freesound.org/people/andrewgnau2/sounds/71534/

`Socket Wrench` by TheGertz
http://freesound.org/people/TheGertz/sounds/131200/

`Socket Wrench` by xxqmanxx
http://freesound.org/people/xxqmanxx/sounds/147018/

`alligator wrench 01.wav` by klankbeeld
http://freesound.org/people/klankbeeld/sounds/198299/

`Violin C-5 Pizzicato Non-Vibrato` by Carlos Vaquero
http://freesound.org/people/Carlos_Vaquero/sounds/153616/

`Violin G-4 Pizzicato Non-Vibrato` by Carlos Vaquero
http://freesound.org/people/Carlos_Vaquero/sounds/153611/

`Pop_9.aif` by SunnySideSound
http://freesound.org/people/SunnySideSound/sounds/67095/

`Pop SFX` by runirasmussen
http://freesound.org/people/runirasmussen/sounds/178446/

`Crash & Glass.wav` by Rock Savage
http://freesound.org/people/Rock%20Savage/sounds/59263/

`splats.wav` by FreqMan
http://freesound.org/people/FreqMan/sounds/42962/

`Door Closing.wav` by ceberation
http://freesound.org/people/ceberation/sounds/235513/

`Metal-Clanging.mp3` by Tiger_v15
http://freesound.org/people/Tiger_v15/sounds/211015/

`Metal_Hit_02.wav` by dheming
http://freesound.org/people/dheming/sounds/197398/

`bolo-hit-tank-self.wav` (from Bolo), Copyright (C) Steuart Cheshire 1993.
A subtle tribute to my favourite Mac game of all-time, hands down. <3
https://en.wikipedia.org/wiki/Bolo_(1987_video_game)
http://bolo.net/
https://github.com/stephank/orona
http://web.archive.org/web/20170105114652/https://code.google.com/archive/p/winbolo/

`Tank fire Mixed.wav` by Cyberkineticfilms (CC0 License, “No Rights Reserved”)
https://freesound.org/people/Cyberkineticfilms/sounds/127845/

`Medals Clanking` by Gareth_H (BY-NC 3.0)
https://freesound.org/people/Gareth_H/sounds/365799/

`Gun/Canon » Auto Assault Rifle/Gun Burst (Outdoor/Close) [Mixed]` by EFlexTheSoundDesigner (BY-NC 3.0)
https://freesound.org/people/EFlexTheSoundDesigner/sounds/393671/

### Images

Gear SVG by Fabián Alexis (CC BY-SA 3.0, https://commons.wikimedia.org/w/index.php?curid=49940470)
https://github.com/fabianalexisinostroza/Antu