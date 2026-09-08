# Contribution #1: Add a svg icon for the crash cymbal

**Contribution Number:** 1  
**Student:** Zamijah Shakeur-Tompkins  
**Issue:** [GitHub issue link](https://github.com/Babali42/DrumBeatRepo/issues/511)  
**Status:** Phase I Complete

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
2. Once setup, clone the repo and cd into DrumBeatRepo/engine/
3. Run sbt fastLinkJS inside directory to set up tools.
4. Open a new terminal and `cd` into `DrumBeatRepo/frontend/`
5. Run `npm run start` within frontend directory 
6. Application loads on a localhost server which you can go to. You will receive a notification to update your NodeJS for Angular if it is out of date.

### Reproduction Evidence

- **Commit showing reproduction:** [Link to commit in your fork]
- **Screenshots/logs:** [If applicable]
- **My findings:** [What you discovered during reproduction]

---

## Solution Approach

### Analysis

[Your analysis of the root cause - what's causing the issue?]

### Proposed Solution

[High-level description of your fix approach]

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** [Restate the problem]

**Match:** [What similar patterns/solutions exist in the codebase?]

**Plan:** [Step-by-step implementation plan]
1. [Modify file X to do Y]
2. [Add function Z]
3. [Update tests]

**Implement:** [Link to your branch/commits as you work]

**Review:** [Self-review checklist - does it follow the project's contribution guidelines?]

**Evaluate:** [How will you verify it works?]

---

## Testing Strategy

### Unit Tests

- [ ] Test case 1: [Description]
- [ ] Test case 2: [Description]
- [ ] Test case 3: [Description]

### Integration Tests

- [ ] Integration scenario 1
- [ ] Integration scenario 2

### Manual Testing

[What you tested manually and results]

---

## Implementation Notes

### Week [X] Progress

[What you built this week, challenges faced, decisions made]

### Week [Y] Progress

[Continue documenting as you work]

### Code Changes

- **Files modified:** [List]
- **Key commits:** [Links to important commits]
- **Approach decisions:** [Why you chose certain approaches]

---

## Pull Request

**PR Link:** [GitHub PR URL when submitted]

**PR Description:** [Draft or final PR description - much of the content above can be adapted]

**Maintainer Feedback:**
- [Date]: [Summary of feedback received]
- [Date]: [How you addressed it]

**Status:** [Awaiting review / Iterating / Approved / Merged]

---

## Learnings & Reflections

### Technical Skills Gained

[What you learned technically]

### Challenges Overcome

[What was hard and how you solved it]

### What I'd Do Differently Next Time

[Reflection on your process]

---

## Resources Used

- [Link to helpful documentation]
- [Tutorial or Stack Overflow post that helped]
- [GitHub issues or discussions that helped]
