---
campanha: 
Jogador: 
tags:
  - personagem
idiomas:
  - comum
link: 
raça: 
ancestralidade: 
profissao: 
grau: 
HP: 
Sanidade: 
percepcao: 
Defesa: 
PontosAegis:
---



<%*  
let title;  
//Pergunta qual o nome da nota
title = await tp.system.prompt("Nome do Personagem");  
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

### História 
- 
- 


### Life Path

#### Traços de Personalidade

#### Aparência

#### Afeição

#### O que você mais valoriza?

#### Sentimentos sobre as pessoas:

#### Pessoa mais Valorizada

#### Objeto mais valioso

#### Background Familiar:

#### Ambiente de infância

#### Crise Familiar

#### Vícios de Doenças

#### Objetivo de vida:

#### Evento trágico



### Ficha e Regras

#### Atributos básicos

- HitPoints (HP):
- Pontos Aegis:
- Defesa: 7 
* Sanidade: 100
* Percepção: 7 

* Intelecto:
> Erudição: 7
> **Inalterabilidade:  7
> Raciocínio: 7

* Fisico:
>Reação: 7
>Força: 7
>Vigor: 7

* Psique:
>Influência: 7 
>**Astúcia: 7 
>Moderação: 7 

- Aegis
>Canalização: 7
<iframe src="_____"   style="width:100%; height:800px;"></iframe>

<iframe src="________"   style="width:100%; height:800px;"></iframe>