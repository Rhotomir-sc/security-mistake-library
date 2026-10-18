# Co-occurrence is not chronological order

Recorded: 2026-10-18. Source: portfolio maintenance review, not a reconstructed claim about an earlier personal lab experience.

## Original state
The original Python script found failures and successes for the same user/IP without comparing timestamps.
[Original file at the reviewed commit](https://github.com/Rhotomir-sc/google-cybersecurity-portfolio-pack/blob/cc6d63ed29735b0b3a324f61d2be474186710f69/integrated-security-case/scripts/analyze_signin_case.py)

## Why it mattered
A success could occur before the failures or outside a meaningful window and still be associated with them.

## Correction
Sort timestamps, require strictly earlier failures in a defined window, group by user and source, and reset after success.
[Current file](https://github.com/Rhotomir-sc/google-cybersecurity-portfolio-pack/blob/main/integrated-security-case/scripts/analyze_signin_case.py)

## Verification
The tests include success before failures, expired failures, different identities/IPs, and unsorted input. Run the linked repository test command.

## Lesson
Describe the operation the evidence actually supports, and make the correction inspectable.
