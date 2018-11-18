---
layout: page
title: Grades
---
This site uses a grading system for instances and types of file bloat, as follows:

- <span class="grade_S">S</span> Exceptionally un-bloated. Kudos to the game developers
- <span class="grade_A">A</span> unremarkable, unbloated, often not mentioned
- <span class="grade_B">B</span> Minor bloat
  - wasting <10% of the space used by the files in question
  - duplicated strings in well-compressed text files
- <span class="grade_C">C</span> Significant bloat
  - wasting 10-50% of space
  - images stored in slightly inappropriate formats (PNG vs TGA)
  - some uncompressible data duplication
- <span class="grade_D">D</span> Extreme bloat
  - wasting 50-99% of space
  - images stored in exceptionally inappropriate formats (SVG vs PNG vs JPG)
  - excessive uncompressible data duplication
- <span class="grade_F">F</span> Unmitigated bloat
  - wasting 99-100% of space
  - entirely unused content
  - large files full of null bytes

Grades for whole games/apps are a sort of weighted average of the problematic grades of the various individual instances of bloat they contain.