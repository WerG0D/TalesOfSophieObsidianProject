---
tags: []
---



<%*  
let title;  

//Pergunta qual o nome da Campanha 
title = await tp.system.prompt("Nome da Campanha");  
await tp.file.rename(title);

//Cria a pastas 
  await tp.file.move("/3. Campanhas/" + title + "/7. Hexcrawl/" ); 

//Cria arquivos  

  tp.file.create_new(tp.file.find_tfile("Nova Página de Objetivos e Personagens"), "_Objetivos dos Personagens", false, "/3. Campanhas/" + title + "/1. Grupo/")

  tp.file.create_new(tp.file.find_tfile("Nova Sessão Zero"), "_Sessão Zero", false, "/3. Campanhas/" + title + "/1. Grupo/")


//Cria Página da Campanha
  tp.file.create_new(tp.file.find_tfile("Nova Página de Campanha"), "_Página de " + title, false, "/3. Campanhas/" + title);

  tp.file.create_new(tp.file.find_tfile("Novo Painel do Mestre"), "_Painel do Mestre", false, "/3. Campanhas/" + title);

  tp.file.create_new(tp.file.find_tfile("Nova Estrutura de Aventura"), "_Estrutura de " + title, false, "/3. Campanhas/" + title);

 tp.file.move("/3. Campanhas/" + title + "/2. Sessões/" ); 
 tp.file.move("/3. Campanhas/" + title + "/3. Facções/" );
 tp.file.move("/3. Campanhas/" + title + "/4. NPCs/" );
 tp.file.move("/3. Campanhas/" + title + "/5. Locais/" );
 tp.file.move("/3. Campanhas/" + title + "/6. Itens/" );

%>


