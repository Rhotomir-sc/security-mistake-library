# A failure count is not a timed burst

Recorded: 2026-10-18. Source: portfolio maintenance review, not a reconstructed claim about an earlier personal lab experience.

## Original state
The C analyzer counted all failed logins but named the flag ioc_failed_login_burst.
[Original file at the reviewed commit](https://github.com/Rhotomir-sc/semester-evidence-packs/blob/5716636ad0af8e0263eca4e0b8f4eb65be199b53/05_Programlama_1/evidence/artifacts/lab01_log_analyzer.c)

## Why it mattered
The program did not parse time or group by identity/IP; a file-wide threshold cannot establish a burst.

## Correction
Rename the metric failed_login_threshold_exceeded and document the scope. Keep time-window detection in the timestamp-aware Python examples.
[Current file](https://github.com/Rhotomir-sc/semester-evidence-packs/blob/main/05_Programlama_1/evidence/artifacts/lab01_log_analyzer.c)

## Verification
Compile and run the C fixture using tools/check_c_example.py; inspect the metric name and expected count. Actual local/CI results belong in the validation record.

## Lesson
Describe the operation the evidence actually supports, and make the correction inspectable.
