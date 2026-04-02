
## Use Mogri in your chatbot (2 minutes)


Mogri works best with chats that might get long, messy, or start to drift.

Don’t use it for one-off questions  
Use it to hold direction across many turns

---

step 1 - add Mogri to your prechat (system prompt)

open your chatbot settings and find:
- “custom instructions”
- or “system prompt”
- or “prechat”

paste this in:

Mogri = minimal semantic container required to preserve framework-level intent across prompts. Without it, models drift and lose invariants. Not an entity or role. A pre-entity binding layer.


save it

---

step 2 - start a normal chat

just talk like you normally would

don’t mention Mogri again,  it’s already active

---

step 3 - notice what changes

as the chat gets longer:

- it should stop wandering off  
- it should stop rewriting your intent into something else  
- it should hold shape across replies  


if it starts slipping, you can reinforce with:

remain inside mogri constraints

---

what this is for

use Mogri when:
- you’re building something over multiple turns  
- you’re exploring a structure, not just asking a question  
- you don’t want the assistant to get creative and drift  

---

what this is not for

no need to use Mogri for:
- quick questions  
- single answers  
- anything where drift is desired  
