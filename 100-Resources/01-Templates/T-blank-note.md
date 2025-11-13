<%*
const title = await tp.system.prompt("Note title:");
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
type: quick-note
tags: []
---
# ${title}

`;
}
%>

