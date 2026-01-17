# SEN-ASSIGNMENT-2
Agwu Nnenna Evergreen 24/13887
Planning / Feasibility
Objective: Build a lightweight, user-friendly password generator
Target users: Anyone needing quick, secure passwords (students, professionals, home users)
Constraints: Pure Python, no external libraries, console only
Success criteria: Generates cryptographically acceptable passwords, easy to use
Estimated effort: 45–90 minutes

Requirements Gathering & Analysis
Functional requirements:
Ask user for desired password length (min 8, max 64)
Options to include/exclude:
Uppercase letters
Lowercase letters
Numbers
Special characters

Generate and display one or multiple passwords
Copy-to-clipboard functionality (optional, using pyperclip if allowed, otherwise just print)
Show strength estimation (very rough)
Non-functional:
Clear prompts and error messages
Prevent generation if no character types selected
Secure random generation (use secrets module instead of random)

System Design
High-level:
One main function to collect preferences
One function to build character pool
One function to generate password using secrets.choice()

Data structures: strings for character sets, list/set for selected types
Input validation loop for length and yes/no choices
Output: clean formatted password + basic info

Implementation
This is the actual coding stage where all processes are written and carried out
Testing
Happy path: Select all character types → length 12 → get mixed password
Edge cases:
Length 8 / 64
Select only one character type → error message & retry
Enter invalid length (7, 65, “abc”)
Ctrl+C during input
Generate many times → randomness check (visually different)


Deployment
Single file: password_generator.py
Run: python password_generator.py
Distribution: GitHub, pastebin, personal blog, email to friends

Maintenance
Possible future changes:
Add clipboard copy (requires pyperclip)
Generate multiple passwords at once
Exclude ambiguous characters (l,1,I,O,0)
Estimate real entropy / strength score
GUI version (tkinter)
