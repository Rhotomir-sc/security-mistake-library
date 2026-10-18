# Documentation paths must match tracked files

Recorded: 2026-10-18. Source: portfolio maintenance review, not a reconstructed claim about an earlier personal lab experience.

## Original state
The module linked to a normal incident-report folder, but the actual folder name had a trailing space. A template link had no target.
[Original file at the reviewed commit](https://github.com/Rhotomir-sc/google-cybersecurity-portfolio-pack/blob/cc6d63ed29735b0b3a324f61d2be474186710f69/06_Module-6_Sound-the-Alarm_Detection-and-Response/README.md)

## Why it mattered
A readable README is not sufficient when its linked evidence cannot be opened.

## Correction
Normalize the report path, add a clearly labeled blank template, and check relative Markdown targets.
[Current file](https://github.com/Rhotomir-sc/google-cybersecurity-portfolio-pack/blob/main/06_Module-6_Sound-the-Alarm_Detection-and-Response/README.md)

## Verification
Run python tools/check_links.py from the repository root. This checks local paths, not external URLs or heading anchors.

## Lesson
Describe the operation the evidence actually supports, and make the correction inspectable.
