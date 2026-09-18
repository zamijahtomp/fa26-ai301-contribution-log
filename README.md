# Contribution #1: Add a svg icon for the crash cymbal

**Contribution Number:** 1  
**Student:** Zamijah Shakeur-Tompkins  
**Issue:** [GitHub issue link](https://github.com/Babali42/DrumBeatRepo/issues/511)  
**Status:** Phase III Complete

---

## Why I Chose This Issue

I chose this issue because I have an interest in UI/UX design and frontend development.

---

## Understanding the Issue

### Problem Description

The crash cymbal object doesn't have a relevant icon which reflects the object's purpose.

### Expected Behavior

There should be a relevant icon for the crash selection.

### Current Behavior

Currently, the icon is a wavelength, not too relevant to a crash cymbal.

### Affected Components

This issue affects the frontend of the application, potentially confusing users on the specific instrument listed, and in turn how to expect to use it.

---

## Reproduction Process

### Environment Setup

Setting up the local environment was very simple, as I only had to install sbt tools, which in turn installed all the dependencies needed for the application. My only challenges faced were wether to install Scala separate from sbt, which you don't, and my NodeJS was outdated for Angular, so I had to update it.

### Steps to Reproduce

1. Install [sbt tools](https://www.scala-sbt.org/) for app dependencies. You do not need Scala if you install sbt.
2. Once setup, clone the repo and `cd` into `DrumBeatRepo/engine/`
3. Run `sbt fastLinkJS` inside directory to set up tools.
4. Open a new terminal and `cd` into `DrumBeatRepo/frontend/`
5. Run `npm run start` within frontend directory 
6. Application loads on a localhost server which you can go to. You will receive a notification to update your NodeJS for Angular if it is out of date.

### Reproduction Evidence

- **Commit showing reproduction:** [https://github.com/shanker-codepath/DrumBeatRepo/tree/cymbal-image](https://github.com/shanker-codepath/DrumBeatRepo/tree/cymbal-image)
- **Screenshots/logs:** <img src='./Screenshot (1556).png' title='Screenshot 1' width='' alt='Screenshot 1' /> <img src='./Screenshot (1558).png' title='Video Walkthrough' width='' alt='Video Walkthrough' />
- **My findings:** 
  - My NodeJS wasn't fully updated
  - I didn't have certain tools, like ng, installed so I got some errors that were quick to fix
  - Pretty easy installation and reproduction overall

---

## Solution Approach

### Analysis

There doesn't seem to be a proper image for the cymbal because there was never one created for it. Within the frontend files there isn't a variable for the `crash` cymbal like there are for `hihats` and `snare`. There also isn't an image for the crash cymbal like there are for the others within the images folder.

### Proposed Solution

Add a new icon for the crash cymbal and add it into the application.

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** For the *Rock* genre, there isn't a proper icon for the `crash` cymbal

**Match:** 
- There are icons for the other instruments in `/frontend/src/assets/images/drums`
- There is code linking the instruments to their icons in `/frontend/src/app/ui/pipes/drum-image.pipe.ts`

**Plan:** 
1. Add crash cymbal variable and image link to `drum-image.pipe.ts`
2. Add crash icons (dark & light) to `images/drums`
3. Update tests

**Implement:** 
- [Crash Icon Code](https://github.com/shanker-codepath/DrumBeatRepo/blob/cymbal-image/frontend/src/app/ui/pipes/drum-image.pipe.ts)
- [Crash Icon Dark](https://github.com/shanker-codepath/DrumBeatRepo/blob/cymbal-image/frontend/src/assets/images/drums/crash-dark.svg)
- [Crash Icon Light](https://github.com/shanker-codepath/DrumBeatRepo/blob/cymbal-image/frontend/src/assets/images/drums/crash-light.svg)

**Review:** [GNU General Public License](https://github.com/Babali42/DrumBeatRepo/blob/main/LICENSE)

**Evaluate:** To evaluate, I will reproduce the issue by going to the genre and should expect to see the updated, correct icon for the crash cymbal.

---

## Testing Strategy

### Unit Tests

- [x] Test case 1: drum-image.pipe.ts returns the correct crash-dark / crash-light icon path when given the crash instrument type, matching the existing pattern used for hihats and snare
- [x] Further test cases not necessary — scope was limited to wiring up an existing icon-lookup pattern for a new instrument type

### Integration Tests

- [x]  Not applicable — the change only adds a new entry to the icon-lookup pipe and two static SVG assets; it doesn't introduce new component interactions to integration-test beyond what the pipe unit test already covers.

### Manual Testing

I tested this manually rather than writing additional automated coverage. I ran the app locally, navigated to the Rock genre, and selected the crash cymbal to confirm the new icon (rather than the old wavelength placeholder) rendered correctly. I checked both the light and dark theme versions to make sure each icon displayed properly and matched the visual style of the other instrument icons (hihats, snare) already in the app.

---

## Implementation Notes

### Week 1 Progress

Set up the local dev environment (sbt for the engine, npm/Angular for the frontend), reproduced the issue, and confirmed there was no existing crash entry in drum-image.pipe.ts or corresponding SVGs in the images folder — matching the pattern already used for hihats and snare.

### Week 2 Progress

Implemented the fix: added the crash variable and icon path to drum-image.pipe.ts, sourced/created matching dark and light SVG icons for the crash cymbal, and dropped them into images/drums. Verified the fix manually by loading the app and selecting the crash cymbal in the Rock genre.

### Code Changes

- **Files modified:** 
  - frontend/src/app/ui/pipes/drum-image.pipe.ts
  - frontend/src/assets/images/drums/crash-dark.svg (new)
  - frontend/src/assets/images/drums/crash-light.svg (new)
- **Key commits:** [cymbal-image branch](https://github.com/shanker-codepath/DrumBeatRepo/tree/cymbal-image)
- **Approach decisions:** Followed the existing convention in the codebase rather than inventing a new pattern — every other instrument has a matching dark/light SVG pair wired into the same pipe, so the crash cymbal just needed to follow that same structure for consistency with the rest of the UI.

---

## Pull Request

**PR Link:** [cymbal-image branch](https://github.com/shanker-codepath/DrumBeatRepo/tree/cymbal-image)

**PR Description:** Not a proper PR, issue had been taken before we could submit, linking working branch instead with commits. Adds a dedicated crash cymbal icon (dark + light variants) and wires it into drum-image.pipe.ts, replacing the generic wavelength placeholder previously shown for the crash cymbal in the Rock genre.

**Maintainer Feedback:**
Submission for this contribution was handled through the course process rather than a direct back-and-forth with the repo maintainer.

**Status:** Submitted

---

## Learnings & Reflections

### Technical Skills Gained

I got more comfortable navigating a mixed Scala/Angular codebase and understanding how a small frontend team structures reusable UI logic — in this case, a single pipe (drum-image.pipe.ts) that centralizes the instrument-to-icon mapping instead of hardcoding image paths in every component. I also practiced designing SVG icons that need to visually match an existing icon set (same style for dark/light themes).

### Challenges Overcome

The trickiest parts were environment setup issues rather than the code change itself — my NodeJS version was too old for the Angular frontend, and I was missing the ng CLI, so I had to fix both before I could even reproduce the issue. Once the environment was working, the actual fix was straightforward since it just followed the existing pattern for other instruments.

### What I'd Do Differently Next Time

I'd double-check my local tooling versions (Node, Angular CLI) against the project's requirements before starting, so I'm not troubleshooting environment issues in the middle of trying to reproduce the bug. I'd also consider writing the pipe unit test as part of the same commit as the fix, rather than treating it as an afterthought.

---

## Resources Used

- [https://www.svgrepo.com/](https://www.svgrepo.com/) — used to find/reference a crash cymbal icon style
- [sbt documentation](https://www.scala-sbt.org/) — used for setting up the engine environment
