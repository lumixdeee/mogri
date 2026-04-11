## On Renaming Mogri

Mogri is not tied to its name.

You can rename it freely. The function does not depend on the label.

What matters is that the name does not collide with anything else already active in the system:

* not a role
* not a variable
* not a framework already in use
* not a common word the model may reinterpret

Avoid names like:

* ring0 (already overloaded in computing)
* your company name (collides with business context)
* descriptive phrases like invariant-drift-reducer (too interpretable, invites mutation)
* human names like Sarah (binds to entity space, breaks pre-entity positioning)

The goal is separation, not meaning.

“Mogri” works because it is effectively isolated. The only real-world overlap is a radish term in Urdu, which is far outside typical model context and does not interfere.

If that overlap matters in your environment, a minimal transformation is recommended:

Irgom

This is simply Mogri reversed:

* preserves structure
* minimizes disruption
* maintains traceability to CSP-106 if needed

More generally:

choose a name that is unused, stable, and does not attract interpretation

---

On “matching the framework name”

The suggestion to rename Mogri to match your framework (e.g. [Meridian]=...) increases coupling.

This has a tradeoff:

* Pro: stronger local binding between name and system
* Con: higher risk of semantic drift, because the name now carries meaning inside the task

Mogri was designed to sit before that layer.

Using the same name for both:

* merges container and content
* reduces separation
* increases the chance the model treats the container as just another concept

So while it can work, it moves away from the original design constraint.

---

On descriptive naming

Names like:
minimal container preserving framework intent

are definitions, not identifiers.

Using them as names:

* increases token load
* invites reinterpretation
* weakens stability across long sessions

Short, opaque identifiers perform better.

---

On recoverability

Even if the original term is lost, the root “mogri” is not arbitrary.

It exists in English through:

* demogrify
* transmogrify

So the form is:

* reconstructible
* searchable
* linkable back to prior definitions

This makes it resilient even under renaming.

---

Summary

* Renaming is fine
* Prefer unused, non-descriptive identifiers
* Avoid collisions with existing domains
* Keep container separate from content
* If needed, use Irgom for minimal disruption

The name is replaceable.
The structure is not.
