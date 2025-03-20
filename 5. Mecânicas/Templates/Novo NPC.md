---
tags:
  - npc
raça: 
profissao: 
local: 
facção: 
PontosAegis: "4"
Defesa: 
HitPoints: 
idiomas: 
campanha:
---
<%*  
let title;  
//Pergunta qual o nome da nota
title = await tp.system.prompt("Nome do NPC");  
await tp.file.rename(title);


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
_%>

###  Apelidos ou Títulos


### Aparência
- 

### Interpretação
- 

### História
- 

### Dados Críticos
- 

### Ficha

#### Status
 
 - HitPoints (HP): 
- Pontos Aegis: 
- Defesa: 
* Sanidade: 100
* Percepção:  

 - Intelecto:
> Erudição: 
> **Inalterabilidade:  
> Raciocínio: 

* Físico:
>Reação: 
>Força: 
>Vigor: 

* Psique:
>Influência: 
>**Astúcia:
>Moderação: 

- Aegis
>Canalização: 

#### Talentos
- 
#### Itens
- 
#### Ataques
- 
#### Aegis

##### Nome da Habilidade: 
- 
##### Categoria 
- 
##### Descrição:
- 
##### Ações da Expressão:

- **Nome da Habilidade **
	- **Tipo de Ação**:
	- **Descrição da ação:**
	- **Condições**
		- **Condição 1:**
		- **Condição 2:**
	- **Pactos:**
		- **Pacto 1:**
		- **Pacto 2:**
