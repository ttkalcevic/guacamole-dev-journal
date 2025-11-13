<%*
const title = await tp.system.prompt("Note title:");
if (!title) {
  tR += "";
} else {
  const date = tp.date.now("YYYY-MM-DD");
  const created = tp.date.now("YYYY/MM/DD HH:mm");
  const newName = `${title}`;
  await tp.file.rename(newName);

  tR += `---
title: "${title}"
created: ${created}
type: knowledge
tags: []
---
# ${title}
`;
}
%>

## Description


## Key points
- 


## Resources
