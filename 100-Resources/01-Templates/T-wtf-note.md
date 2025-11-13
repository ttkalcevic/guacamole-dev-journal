<%*
const title = await tp.system.prompt("WTF?:");
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
type: wtf
tags: [wtf]
---
# 🤯 ${title}`;
}
%>


## WTF just happend?
<!-- Short WTF description -->

## Why is this problem
<!-- Why is this problem or unexpeted? -->

## Lessons / solutions
<!-- What we learned, workarounds ... -->

## Notes
<!-- Any additional notes -->