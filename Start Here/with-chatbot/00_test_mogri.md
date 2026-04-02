## Test Mogri (see the difference yourself)  

To see mogri in action, follow these steps:

---

step 1 - set up a controlled test

open your chatbot in a fresh chat

do NOT add Mogri yet

you are going to run the same task twice:
- once without Mogri  
- once with Mogri  

---

step 2 - run a task that tends to drift

paste something like this:

Build a simple plan over multiple steps.
Keep the same goal throughout.
Do not change the goal.

Start with:
"I want to design a small game about a dragon princess."

then continue the chat for 4–6 messages:
- ask it to expand the idea  
- add constraints  
- change small details  
- refer back to earlier parts  

don’t be careful - just interact normally

---

step 3 - observe failure without Mogri

watch for:

- the goal subtly changing  
- earlier details being forgotten or rewritten  
- tone or structure shifting without reason  
- the assistant introducing new directions you didn’t ask for  

you’ll usually see drift by message 3–5

---

step 4 - reset and enable Mogri

start a NEW chat

open settings and find:
- “custom instructions”
- or “system prompt”
- or “prechat”

paste this:

Mogri = minimal semantic container required to preserve framework-level intent across prompts. Without it, models drift and lose invariants. Not an entity or role. A pre-entity binding layer.

save it

---

step 5 - run the exact same task again

repeat step 2 as closely as possible:
same starting prompt  
same kind of follow-up messages  

---

step 6 - compare behaviour

now watch for differences:

- the goal should stay stable  
- earlier elements should persist  
- changes should fit within what already exists  
- fewer unexpected direction shifts  

if it starts slipping, you can reinforce with:

remain inside mogri constraints

---

what you just did

you ran an A/B test:

A = no Mogri → drift appears  
B = with Mogri → structure holds longer  

---

what this shows

Mogri doesn’t change what the chatbot knows  
it changes how well it holds onto what was already established

---

tip

this effect becomes more obvious:
- the longer the chat   
- the more moving parts you introduce  
- the more you refer back to earlier content  

short chats won’t show much difference
