<%*
const title = await tp.system.prompt("Blocker title:");
if (!title) {
  tR += "";
} else {
  const date = tp.date.now("YYYY-MM-DD");
  const created = tp.date.now("YYYY/MM/DD HH:mm");
  const newName = `${date} - ${title}`;
  await tp.file.rename(newName);

  tR += `---
title: "${title}"
created: ${created}
type: blocker
tags: [blocker]
status: unresolved
---
# 🛑 ${title}
`;
}
%>

## Problem / obstacle
<!-- Short description of blocker / problem -->

## Impact
<!-- How does it impacts work and progress -->

## Next steps / plan
- [ ] Work on solution
- [ ] Ask for help

## Notes
<!-- Other notes, references -->