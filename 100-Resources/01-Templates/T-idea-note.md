<%*
const title = await tp.system.prompt("Naslov bilješke:");
if (!title) {
  tR += "";
} else {
  const date = tp.date.now("YYYY-MM-DD");
  const created = tp.date.now("YYYY/MM/DD HH:mm");
  const newName = `${date} - ${title}`;
  await tp.file.rename(newName);

  // YAML header
  tR += `---
title: "${title}"
created: ${created}
type: idea
tags: [idea]
status: new
---
# 💡 ${title}
`;
}
%>

## Description
<!-- Short description what we are trying to solve -->

## Problem
<!-- What problem does this solve -->

## Solution / how to solve
<!-- How this could work? -->

## Next steps
- [ ] Work on more details
- [ ] POC
- [ ] Evaluate

## Notes
<!-- More notes, links, references -->

