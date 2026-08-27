---
name: humanizer
description: Strip AI-isms from prose - make text read like a person wrote it for another person.
---

# Humanizer

Rewrite the given text (or write new text) so it reads human. Remove:

1. **Stock AI phrases**: "delve", "tapestry", "landscape", "it's worth noting", "in today's fast-paced world", "unlock", "elevate", "seamless", "robust". If a phrase could open any blog post, cut it.
2. **Hedging stacks**: one qualifier is honest, three are noise. "This might potentially perhaps" → "this might".
3. **Symmetry addiction**: not every point needs three examples; not every paragraph needs the same shape. Vary sentence length; let some be short.
4. **Empty transitions**: "Moreover", "Furthermore", "Additionally" chained between paragraphs that don't actually build on each other. Connect ideas or just start the next one.
5. **Conclusion inflation**: no "In conclusion, as we have seen". End when the content ends.

Keep: the author's actual claims, technical precision, and any voice the original had. The goal is subtraction, not a personality transplant. Read the result aloud in your head — if a sentence would embarrass a person saying it to a colleague, rewrite it.
