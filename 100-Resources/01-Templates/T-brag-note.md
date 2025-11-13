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
type: brag
tags: [brag]
---
# 🏆 ${title}

`;
}
%>
### What I did
-  
  
### Impact
-  
  
### Reflection
- 
