#Currenr User Guide:

#Bounce card — clean levels, every time:
 1. Masters bounce in full mode, mobile saves are sketches. This is the actual cause of your level issues, not the float sync: LITE mode has no limiter and runs the compressor 6:1 at −14 dB, so hot input gets baked-in squash before the recorder ever sees it.
 2. Stage at LEVEL ≈ 0.7 with the patch built, then push SING/BLOOM/GRIT — and recheck after. A singing loop is continuous energy, not peaks; it changes the meter after you've already set the level.
 3. The loud test: DRONE chord + ROAR. Peaks should kiss −6 to −3 dBFS, and only the loudest transients should ever touch the limiter (−3 dB in full mode).
 4. Nothing useful lives above −3 dB. The safety tanh and the soft-sat above 0.75 shape anything hotter before the recorder taps the chain — 32-bit float can't rescue it, because the shaping is analog-style and pre-file. Float headroom protects digital overs, not gain staging; the staging is on you.
 5. Recheck after every macro move. Macros push offsets underneath the knobs — RAGE feeds GRIT under it — so a patch that bounced clean can arrive hot without the panel saying why.
