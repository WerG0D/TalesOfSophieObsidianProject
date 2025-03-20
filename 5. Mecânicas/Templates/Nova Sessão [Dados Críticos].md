---
sticker: lucide//file-spreadsheet
banner: "https://i.imgur.com/1slotoI.jpeg"
banner_y: "55"
campanha: 
tags:
  - sessão
data: 
resumo: 
---


<%*  
const hasTitle = !tp.file.title.startsWith("Untitled");  
let title;
let completo;

// Captura o nome da pasta onde o arquivo está localizado
let currentFolderPath = tp.file.folder(true);
let parentFolder = currentFolderPath.split("/").slice(-2, -1)[0];

if (!hasTitle) {  
    // Solicita ao usuário que insira o número da sessão
    title = await tp.system.prompt("Número da Sessão");  
    
    // Renomeia o arquivo com "Sessão X - Pasta"
    await tp.file.rename("Sessão " + title + " - " + parentFolder); 
     completo =  ("Sessão " + title + " - " + parentFolder);

   //Esse código usa a API do Obsidian pra adicionar a tag da campanha nas propriedades
	 tp.hooks.on_all_templates_executed(async () => {
	  const file = tp.file.find_tfile(tp.file.path(true));
	  await app.fileManager.processFrontMatter(file, (frontmatter) => {
    frontmatter["campanha"] = parentFolder;
	  });
	});

} else {  
    title = tp.file.title;  
}  
_%>


## Preparação
- [ ] Revisar Personagens e seus Objetivos Relevantes
- [ ] Preparar Mapas de Batalha, se aplicável
- [ ] Preparar fichas de referências e links

```dataview
TABLE WITHOUT ID
file.link as Personagens
FROM  "3. Campanhas/<% parentFolder %>/1. Grupo" and #Personagem 
WHERE file.name != "Novo Personagem"
```

- [ ] Revisar NPCs importantes
- [ ] Recapitulação das Sessões Passadas

<%*
// Separar o título em partes usando o " - " como separador
let partes = completo.split(" - ");

// Pegar o número da sessão a partir da string "Sessão X"
let sessaoNumero = parseInt(partes[0].split(" ")[1]); // Converte X para um número

// Subtrair 1 do número da sessão
let novaSessaoNumero = sessaoNumero - 1;

// Recriar o título com o novo número da sessão
let novoTitulo = "Sessão " + novaSessaoNumero + " - " + partes[1];
_%>

![[<% novoTitulo %>#Resumo da Sessão]]

## Início Forte
-  

## Lista de Revelações
### Revelação 1
- [ ] 
- [ ] 
- [ ] 
### Revelação 2
- [ ] 
- [ ] 
- [ ] 
### Revelação 3
- [ ] 
- [ ] 
- [ ] 

## Cenas 
- 
- 
-  
  
## NPCs
- 
- 
- 

## Bloco de Notas
- 
- 

# Depois do jogo
- [ ] Fazer um resumo da sessão. Mais completo abaixo e de uma linha nas propriedades da notas
- [ ] Verificar Facções e os relógios de objetivos
- [ ] Pergunte aos jogadores quais objetivos eles pretendem perseguir na próxima sessão

### Faltantes
- 

## Resumo da Sessão
