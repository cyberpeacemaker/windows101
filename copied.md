Your understanding is correct, and the sentence you quoted is *not* really misleading, but it *can* be clearer.

Here’s the accurate picture:

### ✅ What a Global Catalog (GC) actually contains

A **Global Catalog server** stores:

* **A *partial* attribute set (PAS)** for *every* object in the forest (from all domains)
  → This includes only selected attributes that are useful for searching and locating objects (e.g., names, group memberships, email addresses).
* **A *full* attribute set** for all objects in the domain where the GC is also a domain controller.

So yes — globally, it stores *partial* data for objects in other domains.

### Why the wording you quoted may sound confusing

> “a partial, read-only copy of all the objects in a multiple-domain forest”

This is technically correct because:

* **The copy *is* partial** → only the PAS is replicated between domains.
* **It *is* read-only** → attributes from other domains cannot be modified on the GC.

But it may mislead someone into thinking that the GC stores *complete* objects or that it only contains partial copies even for its own domain (which is not true).

### A clearer way to phrase it

A better description would be:

> *A global catalog server stores a full replica of all directory objects in its own domain and a partial, read-only replica of selected attributes for all objects in the rest of the forest.*

### Bottom line

You are right:
✔ The GC contains **partial** data from other domains — enough for indexing and locating objects.
✔ The quoted sentence is technically correct but could be phrased more clearly to avoid confusion.

If you want, I can rewrite the whole definition in a clearer, documentation-ready format.
