# Developer Log (DEVLOG.md)
## Monopoly Board Simulator (Spring 2026)

Minimum **6 entries** required.

Each entry must document learning and reasoning. Fabricated bugs are not expected.

---

## Allowed Entry Types
Each entry may be one of the following:

1) **Bug Fix Entry**
- The issue encountered.
- Error messages or symptoms.
- Attempts made.
- Final resolution.

2) **Edge Case / Testing Entry**
- A failure discovered through testing.
- The specific input/state that caused it.
- The change you made to handle it correctly.

3) **Engineering Decision Entry (up to 2 allowed)**
- A design decision you made.
- An alternative approach you considered.
- Why you chose one approach over another (tradeoffs).

---

### Entry 1
**Date:** 2026-02-27 
**Entry Type:** Bug Fix 
**Task worked on:**  
addSpace function.
**Issue or decision:**  
When writing code, the code was greyed out like it was commented out, but wasn’t a comment.
**Error message / symptom (if applicable):**  
**What I tried:**  
When typing something random in the function, for example, I put e somewhere, it would get its color back.
I wasn't sure why though.
**Fix / resolution (or final decision):**  
if (nodeCount = MAX_SPACES) {
return false;
}
This was my code, and I missed the fact that I used = and not == for the condition. After putting the second equal sign
the color returned.
**Commit(s):**  

---

### Entry 2
**Date:** 2026-03-03
**Entry Type:** Testing Entry 
**Task worked on:**  
AddMany function.
**Issue or decision:**  
The if statement uses addSpace(value) as a condition and then has addSpace(value) 
if it returns true inside the if statement. 
This adds a space twice, which was not the intended use for using addSpace as the condition, 
as I wanted it to check if it could addSpace before adding a space.
**Error message / symptom (if applicable):**
**What I tried:**  
I tried removing the addSpace from the if statement cause it already adds a space,
and it returns false if the list is full from the addSpace function.
**Fix / resolution (or final decision):**  
Removing the addSpace within the if statement worked. 
I also added a break so it gets out of the loop if the list is already full,
so it doesn’t add spaces anymore.
**Commit(s):**  

---

### Entry 3
**Date:** 2026-03-04  
**Entry Type:** Engineering Decision  
**Task worked on:**  
countSpaces function.
**Issue or decision:**  
Used do while loop instead of just while loop.
**Error message / symptom (if applicable):**  
**What I tried:** 
Intended to use while loop to iterate through the list all the way up to tail and
then when the loop stops I increment it one more time so it counts tail.
**Fix / resolution (or final decision):**  
I used a do while so I could increment and count the space it's currently on and changed 
the condition for the loop to stop at head so it can count tail without 
having to increment spaces outside the loop.
**Commit(s):**  

---

### Entry 4
**Date:** YYYY-MM-DD  
**Entry Type:** Bug Fix / Edge Case / Engineering Decision  
**Task worked on:**  
**Issue or decision:**  
**Error message / symptom (if applicable):**  
**What I tried:**  
**Fix / resolution (or final decision):**  
**Commit(s):**  

---

### Entry 5
**Date:** YYYY-MM-DD  
**Entry Type:** Bug Fix / Edge Case / Engineering Decision  
**Task worked on:**  
**Issue or decision:**  
**Error message / symptom (if applicable):**  
**What I tried:**  
**Fix / resolution (or final decision):**  
**Commit(s):**  

---

### Entry 6
**Date:** YYYY-MM-DD  
**Entry Type:** Bug Fix / Edge Case / Engineering Decision  
**Task worked on:**  
**Issue or decision:**  
**Error message / symptom (if applicable):**  
**What I tried:**  
**Fix / resolution (or final decision):**  
**Commit(s):**  
