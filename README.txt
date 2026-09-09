
PROACT1102 V2
=============

Adds:
- Employee / Manager / Admin roles
- Manager view of all reports
- Corrective actions
- Automatic recurring-risk pattern alerts
- Existing Supabase login and report database

INSTALL
-------
1. Keep your current connected index.html backup.
2. In Supabase SQL Editor, run PROACT1102_v2_upgrade.sql.
3. To make your account a manager:
   - Supabase > Authentication > Users
   - copy your user UUID
   - SQL Editor:
     update public.profiles set role = 'manager' where id = 'YOUR-UUID';
4. Rename PROACT1102_v2_index.html to index.html.
5. Upload it to your GitHub PROACT repository and replace the current index.html.
6. Commit changes and wait for GitHub Pages to redeploy.

PATTERN RULES
-------------
PROACT1102 flags a repeat risk when the same Location + Risk Category occurs:
- 3 or more times in the last 30 days, OR
- 5 or more times in the last 90 days.

DEMO ONLY
---------
Continue to use fake/test data only until organisational approval, privacy/security controls,
retention rules, and production authentication have been agreed.
