---
status: ativa
campanha:
---
<%*  
// Captura o nome da pasta onde o arquivo está localizado
let currentFolderPath = tp.file.folder(true);
let parentFolder = currentFolderPath.split("/").slice(-2, -1)[0];

//Esse código usa a API do Obsidian pra adicionar a tag da campanha nas propriedades
	 tp.hooks.on_all_templates_executed(async () => {
	  const file = tp.file.find_tfile(tp.file.path(true));
	  await app.fileManager.processFrontMatter(file, (frontmatter) => {
    frontmatter["campanha"] = parentFolder;
	  });
	});
%>


# Nome da Campanha

## Personagens
```dataview
TABLE WITHOUT ID link(file.name) AS "STATUS", Jogador, PP, CA, infravisao as Infravisão, idioma as Idiomas
FROM "3. Campanhas/<% await tp.file.folder(false) %>/1. Grupo" and #Personagem 
```

## Sessões

```meta-bind-button
label: Criar Nova Sessão [Dados Críticos]
icon: "clipboard-list"
hidden: false
class: ""
tooltip: Clique para cirar uma Nova Sessão de Jogo no Modelo do Dados Críticos
id: novasessaodados
style: default
actions:
  - type: templaterCreateNote
    templateFile: 5. Mecânicas/Templates/Nova Sessão [Dados Críticos].md
    folderPath: 3. Campanhas/<% await tp.file.folder(false) %>/2. Sessões
    fileName: ""
    openNote: true
```

```dataview
TABLE WITHOUT ID file.link as Sessão, resumo as "Resumo" from "3. Campanhas/<% await tp.file.folder(false) %>/2. Sessões"
SORT sessionNum ASC
```


## Verdades sobre o Mundo
*Escreva algumas verdades ou fatos interessantes sobre o mundo. Podem ser as definidas na sessão zero ou aquelas que surgirem durante a mesa*
- 


## Facções

```dataview
TABLE WITHOUT ID file.link as Facção, resumo as "Descrição" 
from "3. Campanhas/<% await tp.file.folder(false) %>/3. Facções"
```

## Regras da Casa
- 

## Ferramentas de Segurança