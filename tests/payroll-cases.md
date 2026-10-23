# Manual regression cases

1. Payroll period 2026-11 includes 2026-10-21 through 2026-11-20.
2. Night shift date 2026-10-21 22:00 to 2026-10-22 06:00 is one record.
3. Saturday morning present, no unpaid leave in cycle => 2.5 overtime hours.
4. Saturday afternoon present, no unpaid leave in cycle => 2.5 overtime hours.
5. Saturday night => 0 automatic overtime hours.
6. Saturday morning with qualifying unpaid leave in cycle => 0 overtime.
7. Saturday afternoon with qualifying unpaid leave in cycle => 0 overtime.
8. Unpaid leave deduction = qualifying days * wage base / configured divisor.
9. Missing basic salary blocks calculation.
10. Divisor 0 blocks calculation.
11. Employee meal allowance = eligible attendance days * configured meal rate.
12. THP = total earnings - total deductions.
13. Backup restore with malformed JSON is rejected.
14. Duplicate same-date attendance prompts replacement.
