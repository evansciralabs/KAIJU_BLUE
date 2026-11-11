# Bounce card — clean levels, every time

(Before you read this: OUT tab > Level -6 or -10dB are my preferred starting points. The rest of this information hints to that, rants about dead code and beats around the bush saying you need to set the level but then used .7 as a reference. When you adjust LEVEL in the OUT tab a toast appears showing you the dB adjustment.)

1. Masters bounce in full mode, LITE saves are sketches. LITE is any
   coarse-pointer device or a ?lite URL — it runs the compressor 6:1 at
   −14 dB with no limiter, so hot input gets baked-in squash before the
   recorder ever sees it. Full mode runs 3:1 at −20 dB (soft knee) with a
   −3 dB limiter behind it. Note: the recorder taps AFTER the whole chain
   in both modes — the file is always what you hear, never raw gain.

2. Stage at LEVEL ≈ 0.7 with the patch built, THEN push SING/BLOOM/GRIT
   — and recheck after. A singing loop is continuous energy, not peaks:
   it settles after the attack and can sit hotter than the level you set.
   There is no peak meter in the app — verify against the bounced file.

3. The loud test: DRONE chord + ROAR. Peaks should kiss −6 to −3 dBFS,
   and only the loudest transients should touch the limiter (−3 dB in
   full mode). Sustained notes pinning the limiter = pull LEVEL down.

4. The ceiling is −3.1 dBFS, by design — not by taste. The recorder taps
   after the safety tanh (0.7·tanh(x/0.7)), which caps the file at 0.70.
   The "soft-sat above 0.75" stage behind it never engages — its knee
   sits above the tanh's ceiling — so the tanh is the whole story.
   32-bit float can't rescue anything: the shaping is analog-style and
   pre-file. Float headroom protects the resample and the fades, not
   gain staging; the staging is on you.

5. Recheck after every macro move — the panel DOES tell you why. Knobs
   show effective values, so RAGE visibly drives GRIT (and RES / TREMOLO /
   GRIT DRV) up, DREAD pushes the REVERB and ECHO sends, GHOST pushes
   ENSEMBLE. The danger is a clean-bouncing patch re-staging itself under
   a macro — not that it hides. Watch SENDS while you ride macros.

6. Two bounce killers live in the recorder, not the mix:
   • Output sustained above −7 dBFS RMS for ~1.2 s trips the hot-guard —
     the engine flushes MID-TAKE ("safety cut") and your bounce goes
     silent from that point.
   • ONE-SHOT only auto-stops after it has seen the signal above −50 dB
     RMS at least once, then 0.6 s below −62 dB ends the take. Quieter
     than −50 dB and it never arms — the take runs to the LEN cap and
     gets the 1.5 s cap-fade (the * in TAKES).
