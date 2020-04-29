# UniversalPaperclipsSavegame
Code to save and load a universal paperclips game

let message = '';
message += "/*COPY THIS CODE TO RESTORE THE CURRENT GAME*/\n";
save()
for (let i = 0; i < localStorage.length; ++i) { 
  message += `let a${i} = ` + localStorage.getItem(localStorage.key(i)) + `;`;
  message += `localStorage.setItem("${localStorage.key(i)}", JSON.stringify(a${i}));`;
}
message += `load()`;
console.log(message);
