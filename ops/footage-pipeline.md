# Footage: naming, offload, backup

**This is the only process in `ops/` where a mistake is unrecoverable.** A wrong price gets corrected. A lost card does not come back, and neither does the day, the people, or the light.

**The rule, in one line: footage exists in two physical places before anyone leaves the location, and in three before the week ends.**

---

## Offload, on the day, every day

**Before anyone goes home. Not that evening, not tomorrow.**

| # | Step | Why this order |
|---|---|---|
| 1 | **Copy the card to the working drive.** Copy, do not move | Move deletes the only other copy mid-transfer |
| 2 | **Copy the working drive to the second drive** | Two places |
| 3 | **Open three clips from the second drive and watch them** | A copy you have not opened is a hope, not a backup |
| 4 | **Only now format the card, and format it in the camera** | Formatting in a computer is how cards get corrupted |
| 5 | **The second drive leaves the building with a different person** | One flat, one fire, one burglary, one flood. **Two drives in one bag is one copy** |

**If step 3 fails, nobody formats anything.** Shoot the next day on a new card and work out what happened with the footage still on the original.

### Within the week: the third copy

**Upload the selects to cloud storage.** Not the whole card, the selects and every piece to camera. A film in progress with no off-site copy is one dropped bag from being re-shot.

> **BOARD: pick and pay for one cloud storage account before the first shoot.** Two 4K shoot days is a real amount of data and the free tiers will not hold it. **This is a small recurring cost that prevents the one failure that cannot be fixed.**

---

## Naming

**One pattern. No exceptions, because the exception is the file nobody can find in March.**

```
EP02_2027-01-14_makati-market_A_001.mp4
 |      |            |          |   |
 code   date      location   angle shot
```

| Part | Rule |
|---|---|
| **Code** | `EP01` to `EP05`. **`UNSORTED` if it does not belong to a film yet.** Never blank |
| **Date** | `YYYY-MM-DD`. Sorts correctly, reads the same in every country |
| **Location** | Lowercase, hyphens, the neighbourhood. **`standards.html` promises the district is named, so the file should know it too** |
| **Angle** | `A` and `B`. The kit requires two angles on every interview |
| **Shot** | Three digits, from the camera if it gives useful ones |

**Audio recorded separately gets the same name with `_AUD`.** Clean street sound gets `_ROOM`, since `kit/README.md` requires sixty seconds per location and those files are the ones that get lost.

### The folders, made before the first shoot and never improvised

```
vaya-footage/
  EP01-block-by-block/
    01-footage/
    02-audio/
    03-releases/      <- photographed, named after the person
    04-selects/
    05-exports/
  EP02-visa-truth/
  ...
  UNSORTED/           <- empty it every Friday or it becomes the archive
  _releases-blank/    <- the PDF, so anyone can print more
```

**`03-releases` sits inside the episode folder on purpose.** A release in a different system from the footage it covers is a release nobody will find when it matters.

---

## Releases: the paperwork that makes footage usable

**`standards.html` says nobody appears without agreeing to, and `briefs/README.md` says blanks in the bag every day.** The process:

| # | Step |
|---|---|
| 1 | **Signed before the first frame.** Not after the good take |
| 2 | **Photographed on the spot**, both sides, in focus |
| 3 | **Filed in `03-releases/` named after the person**, same day as the offload |
| 4 | **The blur or withhold choice is copied into the episode brief**, because the editor will not read the release |
| 5 | **No release, no footage used.** Either contractor can enforce this with no escalation |

**The one that catches people out:** someone who wanders into a wide shot and is recognisable. **Either get the release or lose the shot.** A busy market wide is usually fine; a person who is clearly the subject of the frame is not.

---

## What to check before the shoot, not after

A thirty-second list, and it has saved every production that has ever used one.

- **Cards formatted, in the camera, this morning**
- **Batteries, all of them, and the charger in the bag**
- **Audio: the recorder, the lav, spare batteries for the lav specifically.** `briefs/00` already says audio first, camera last
- **Both drives in the bag, and they are not both going home with the same person**
- **Twenty blank releases and two pens**
- **The episode brief, on paper or on a phone that is not the camera**

## Accept when

A stranger could open `vaya-footage/`, find every frame of EP02, find the release for every face in it, and tell you which angle and which day each clip came from, **without asking anyone.**
