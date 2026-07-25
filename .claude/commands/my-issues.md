---
model: haiku
description: Check status of my open issues on rtk-ai/rtk
---

# /my-issues

Check the current status of issues I (Rmohid) have filed on rtk-ai/rtk.

## Instructions

1. Fetch all issues created by Rmohid (excluding pull requests):
   ```
   gh api "repos/rtk-ai/rtk/issues?creator=Rmohid&state=all&per_page=100" --jq '.[] | select(.pull_request == null)'
   ```

2. Display a table with columns: Number, State (open/closed), Title, Labels

3. Highlight any issues that were recently closed (check `closed_at` date).

4. If any issues are closed, check if the fix was included in a release by looking at recent tags/releases.

5. Summary: count of open vs closed issues.
