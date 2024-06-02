<%*
const file = tp.file.find_tfile(tp.date.now("YYYY-MM-DD"))
if (file) {
    const loggedItem = await tp.system.prompt("发生什么事了？")
    const time = tp.date.now("HH:mm")
    let content = (await app.vault.read(file)).split("\n")
    const index = content.indexOf("## 行云")

    if (index !== -1) {
        // 找到小标题后，检查下面的行，直到找到一个时间更晚的条目或到达文件末尾
        let insertionIndex = index + 1;
        while (insertionIndex < content.length && content[insertionIndex].startsWith("- ")) {
            const lineTime = content[insertionIndex].substring(2, 7);
            if (time < lineTime) break;
            insertionIndex++;
        }
        content.splice(insertionIndex, 0, `- ${time} - ${loggedItem}`);
    } else {
        // 如果没有找到小标题，将其添加到文件末尾
        content.push("## 行云", `- ${time} - ${loggedItem}`);
    }
    await app.vault.modify(file, content.join("\n"))
} else {
    new Notification("No Daily Note Found!")
}
-%>
