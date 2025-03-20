---
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

# Objetivos de Curto Prazo
- [ ] **Personagem**: descrição do objetivo
- [ ] 
- [ ] 
- [ ] 
- [ ] 
- [ ] 

# Objetivos de Médio Prazo
- [ ] 
- [ ] 
- [ ] 
- [ ] 
- [ ] 


# Objetivos de Longo Prazo
- [ ] 
- [ ] 
- [ ] 
- [ ] 
- [ ] 
- [ ] 
