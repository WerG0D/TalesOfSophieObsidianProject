---
status: ativa
campanha:
---



# Nome da Campanha

## Personagens
```dataview
TABLE WITHOUT ID link(file.name) AS "STATUS", Jogador, PP, CA, infravisao as Infravisão, idioma as Idiomas
FROM "3. Campanhas/Eldoria RPG/1. Grupo" and #Personagem 
```

## Sessões

```meta-bind-button
label: Criar Nova Sessão
icon: "clipboard-list"
hidden: false
class: ""
tooltip: Clique para cirar uma Nova Sessão de Jogo no Modelo do Dados Críticos
id: novasessaodados
style: default
actions:
  - type: templaterCreateNote
    templateFile: 5. Mecânicas/Templates/Nova Sessão [Dados Críticos].md
    folderPath: 3. Campanhas/Eldoria RPG/2. Sessões
    fileName: ""
    openNote: true
```

```dataview
TABLE WITHOUT ID file.link as Sessão, resumo as "Resumo" from "3. Campanhas/Eldoria RPG/2. Sessões"
SORT sessionNum ASC
```


## Facções

```dataview
TABLE WITHOUT ID file.link as Facção, resumo as "Descrição" 
from "3. Campanhas/Eldoria RPG/3. Facções"
```
