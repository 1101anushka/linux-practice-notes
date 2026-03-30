Text Processing Tools in Linux (grep, sed, awk)

Overview

These tools are widely used in DevOps for:
- Log analysis
- Data filtering
- Text transformation
- Automation scripts


1. grep (Global Regular Expression Print)

Purpose: Search for patterns inside files

Basic Syntax

grep "pattern" file.txt

🔥 Examples
grep "error" logs.txt

Finds lines containing "error"

grep -i "error" logs.txt

Case-insensitive search

grep -n "error" logs.txt

Shows line numbers

grep -r "error" .

Search recursively in directory

🧠 Use Case
Finding errors in logs
Searching keywords in files


2. sed (Stream Editor)
Purpose: Edit/transform text without opening file

Basic Syntax
sed 's/old/new/' file.txt

Examples
sed 's/error/warning/' file.txt

Replaces first occurrence in each line

sed 's/error/warning/g' file.txt

Replaces all occurrences

sed -i 's/error/warning/g' file.txt

Edits file directly

sed -n '1,5p' file.txt

Prints lines 1 to 5

🧠 Use Case
Replacing values in config files
Cleaning logs
Automating edits


3. awk
Purpose: Process structured data (columns)

Basic Syntax
awk '{print $1}' file.txt

🔥 Examples
awk '{print $1}' file.txt

Prints first column

awk '{print $1, $3}' file.txt

Prints multiple columns

awk -F "," '{print $1}' file.csv

Uses comma as delimiter

awk '{sum += $1} END {print sum}' numbers.txt

Calculates sum

🧠 Use Case
Working with CSV/log files
Extracting specific columns
Data processing


⚔️ DIFFERENCE BETWEEN grep vs sed vs awk
Tool	Purpose   	   Works On	    Modification
grep	Search text	   Lines	        ❌ No change
sed	  Edit text	     Stream	        ✅ Modify
awk	  Process data	 Columns	      ✅ Advanced


🔥 SIMPLE UNDERSTANDING
grep → 🔍 Find something
sed → ✂️ Replace/edit something
awk → 📊 Analyze data


🧠 REAL DEVOPS EXAMPLES
Find errors in logs: grep "ERROR" app.log
Replace IP in config: sed -i 's/127.0.0.1/192.168.1.1/g' config.txt
Extract column from logs: awk '{print $2}' access.log
