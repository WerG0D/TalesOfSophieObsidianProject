---
tags:
  - facção
resumo:
---
<%*  
let title;  

//Pergunta qual o nome da Facção 
title = await tp.system.prompt("Nome da Facção");  
await tp.file.rename(title);

let currentFolderPath = tp.file.folder(true);
let parentFolder = currentFolderPath.split("/").slice(-2, -1)[0];

%>

#### Grau  

 
#### Descrição

#### Liderança  
- 

> [!infobox]
> # Símbolo ou Imagem
> ![[ImagePlaceholder.png]]
> ###### Membros / Agentes
> ```dataview
TABLE WITHOUT ID
file.link as Membros
FROM  "3. Campanhas/<%  parentFolder %>/4. NPCs" or "3. Campanhas/<%  parentFolder %>/1. Grupo" 
WHERE facção = "<% title %>"


##### Aliados
- 

##### Inimigos 
- 
  
##### Objetivos
| Passos        | Objetivos            Rolar: `dice: d6` |
| ------------- | -------------------------------------- |
| `clock 1 / 5` |                                        |
| `clock 1 / 5` |                                        |
| `clock 1 / 5` |                                        |


