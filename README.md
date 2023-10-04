---announcement
hidden: false

---

refine Devtools beta version has been released, join the waitlist to try it out. https://s.refine.dev/devtools

---

---announcement
hidden: false

---

Hello from refine team! Hope you enjoy! Join our Discord community to get help and discuss with other users. https://discord.gg/refine


---

---announcement
hidden: false

---
```ts
const parseAnnouncement = (raw: string): Announcement => {
    const fixed = raw.replace(ANNOUNCEMENT_DELIMITER, "---");
    const parsed = matter(fixed);
    const content = (
        parsed.content.length === 0
            ? fixed.replace(/---/g, "")
            : parsed.content.replace(/---/g, "")
    ).trim();

    return {
        ...parsed.data,
        content,
    } as Announcement;
};
```
---


