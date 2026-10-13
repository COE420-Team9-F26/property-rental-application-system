# Critical Path

**Critical Path:** T1 → T2 → T3 → T5 → T6 → T8 → T11 → T13 → T15 → T16

**Expected Project Duration:** 3 + 3 + 4 + 6 + 6 + 7 + 4 + 7 + 3 + 3 = **46 days**

## Explanation
We got the critical path from the forward and backward passes in the network schedule. Going forward, each task could only start after its slowest predecessor was done, which put the earliest project finish at day 46. We then worked backwards from day 46 to find the latest each task could start without pushing the deadline, and subtracted to get the slack.

The tasks with zero slack are the ones on the critical path. None of them has any room to slip, so if one is late the whole project is late. They also make up the longest chain in the network, adding up to exactly 46 days. T9 and T10 only have 1 day of slack each, so they need watching.

## Verification
We entered the same tasks, durations and dependencies into ProjectLibre. It finished the project on 15 Dec 2026 (46 working days from 13 Oct) and flagged the same tasks as critical. See `Critical_Path/projectlibre-table.png` and `Critical_Path/projectlibre-gantt.png`.
