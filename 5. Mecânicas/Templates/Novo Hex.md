---
tags:
  - hex
terreno:
  - planície
clima:
  - temperado
região: 
periculosidade:
  - normal
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
_%>

# Nome
> [!Descrição]
> Descrição Geral do Hex

### Subhexes: 

- [ ]    **1**   Descrição
- [ ]    **2** 
- [ ]    **3**  
- [ ]    **4** 
- [ ]    **5** 
- [ ]    **6** 
- [ ]    **7** 


> [!infobox]+
> # Subhex
>
> > [!grid|masonry]
>  ![[subhexesnumeros.png|cover htiny ]]
> ###### Info
> | Periculosidade do Hex |
> | ---- |
> | [ Normal :: 1 em 6]  | 
> | [ Perigoso :: 2 em 6  ] | 
> | [ Extremo :: 3 em 6 ] |
> | **Dados de Encontro** |
> | [ d6 :: Planície, Colina]  | 
> | [ d8 :: Deserto, Geleira, Pântano]  | 
> | [ d10 :: Floresta, Montanha]  | 

