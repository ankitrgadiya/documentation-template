---
layout: default
group: usage
permalink: /usage/revision-history/
---

This new update adds Revision History feature in the template. This is inspired
by <a href="https://tldp.org">TLDP</a>'s documentations.

This is very easy to use. Each time new revision comes out, just add the details
in `./_data/revision.yml`. The format is very simple:

```
- revision: REVISION_NUMBER
  date: DATE
  revised-by: AUTHOR
  email: AUTHOR_EMAIL
```

If you don't wanna use this feature then just remove the `revision.yml` file
from `./_data/` directory.

That's it.
