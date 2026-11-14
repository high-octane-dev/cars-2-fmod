# Cars 2: The Video Game (Arcade) FMOD Decompilation

This project aims to decompile the FMOD event banks (`.fev` files) from the Arcade version of *Cars 2: The Video Game* into `.fdp` project files, enabling advanced audio modding.

Since crude recreations of the original event banks usually sound very wrong in-game, it is crucial to have a strong, highly accurate base for modding. By meticulously analyzing the binary `.fev` files and grafting that data back into a manual recreation, it is possible to build an `.fdp` that compiles down to a byte-identical `.fev`; this is the core principle behind this project.

## Requirements

To work with or compile these project files, use **FMOD Designer Ver. 4.32.9**. For compiling to equivalent targets to vanilla, use **FMOD Designer Ver. 4.28.5** for the three older `v0x3d` banks: `imusic.fev`, `Multichannel_test.fev`, and `ui.fev`. All `.fdp` project files are located in `xbox_ps3_dx/` so that all relative waveform paths (`sfx/...`, `streamstereo/...`, `../xbox_ps3_dx/...`, `../wii/...`, and `../sfx/...`) resolve cleanly inside the repository.

## Current Progress

- [X] `Breakables.fev` (Matching!)
- [X] `CarBody.fev` (Matching!)
- [X] `emusic.fev` (Matching!)
- [X] `frontend.fev` (Matching!)
- [X] `gameplay.fev` (Matching!)
- [ ] `holocars_skidpad.fev` / `holodhart.fev` (Decompiled — exact size `6,060` bytes with FMOD Designer 4.19.0; 100% byte-identical across all `6,059` data bytes, differing only in the 1-byte FEV version header `0x35` from FMOD Designer 4.18.x vs `0x36` in 4.19.0; internal project name is `holodhart`)
- [X] `imusic.fev` (Matching! 100% byte-exact with FMOD Designer 4.28.5)
- [X] `LevelAirport.fev` (Matching!)
- [X] `LevelItaly.fev` (Matching!)
- [X] `LevelLondon.fev` (Matching!)
- [X] `LevelOilRig.fev` (Matching!)
- [X] `LevelRadiatorSprings.fev` (Matching!)
- [X] `LevelTokyo.fev` (Matching!)
- [X] `LevelTutorial.fev` (Matching!)
- [X] `loadingairport.fev` (Matching! 100% byte-exact)
- [X] `loadingfrontend.fev` (Matching! 100% byte-exact)
- [X] `loadingitaly.fev` (Matching! 100% byte-exact)
- [X] `loadinglondon.fev` (Matching! 100% byte-exact)
- [X] `loadingoilrig.fev` (Matching! 100% byte-exact)
- [X] `loadingradiatorsprings.fev` (Matching! 100% byte-exact)
- [X] `loadingtokyo.fev` (Matching! 100% byte-exact)
- [X] `menu.fev` (Matching!)
- [X] `Multichannel_test.fev` (Matching! 100% byte-exact with FMOD Designer 4.28.5)
- [X] `program.fev` (Matching! 100% byte-exact)
- [X] `reverb.fev` (Matching! 100% byte-exact)
- [X] `surfacetype.fev` (Matching!)
- [X] `ui.fev` (Matching! 100% byte-exact with FMOD Designer 4.28.5)
- [ ] `VehicleEngine.fev` (Decompiled — exact size `23,835` bytes; 7 bytes differ in GUI-stale `num_envelopes` counter on `load` parameter)
- [ ] `VehicleEngine1.fev` (Decompiled — exact size `55,005` bytes; 2 bytes differ in GUI-stale `num_envelopes` counter on `load` parameter)
- [X] `Weapons.fev` (Matching!)