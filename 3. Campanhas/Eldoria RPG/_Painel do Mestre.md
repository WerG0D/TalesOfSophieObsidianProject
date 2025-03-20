---
campanha: 
banner: "https://i.imgur.com/1slotoI.jpeg"
banner_y: "100"
banner_x: 0.5
---

```dataview
TABLE WITHOUT ID link(file.name) AS "Personagem",  Jogador
FROM "3. Campanhas/Eldoria RPG/1. Grupo" and #personagem 
```
 
```dataview
TABLE WITHOUT ID link(file.name) AS "STATUS", raça AS Raça, ancestralidade AS Ancestralidade, profissao AS Profissão, grau AS Grau, HP, Sanidade, percepcao AS Percepção, Defesa, PontosAegis
FROM "3. Campanhas/Eldoria RPG/1. Grupo" and #personagem 
WHERE file.name != "_Painel do Grupo"
```

```dataview
TABLE WITHOUT ID link(file.name) AS "IDIOMAS", idiomas as Idiomas
FROM "3. Campanhas/Eldoria RPG/1. Grupo" and #personagem 
WHERE file.name != "_Painel do Grupo"
```

```meta-bind-button
label: Criar Novo Personagem
icon: "user"
hidden: false
class: ""
tooltip: Clique para cirar um novo personagem neste grupo
id: criarnovopersonagem
style: primary
actions:
  - type: templaterCreateNote
    templateFile: 5. Mecânicas/Templates/Novo Personagem.md
    folderPath: 3. Campanhas/Eldoria RPG/1. Grupo
    fileName: ""
    openNote: true

```
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
```meta-bind-button
label: Criar Nova Sessão [Mestre Preguiçoso]
icon: "clipboard-list"
hidden: false
class: ""
tooltip: Clique para cirar uma Nova Sessão de Jogo no Modelo do Dados Críticos
id: novasessaolazy
style: primary
actions:
  - type: templaterCreateNote
    templateFile: 5. Mecânicas/Templates/Nova Sessão [Mestre Preguiçoso].md
    folderPath: 3. Campanhas/Eldoria RPG/2. Sessões
    fileName: ""
    openNote: true
```
```meta-bind-button
label: Criar Nova Facção
icon: "users"
hidden: false
class: ""
tooltip: Clique para cirar uma Nova Facção
id: novafaccao
style: default
actions:
  - type: templaterCreateNote
    templateFile: 5. Mecânicas/Templates/Nova Facção.md
    folderPath: 3. Campanhas/Eldoria RPG/3. Facções
    fileName: ""
    openNote: false
```
```meta-bind-button
label: Criar Novo NPC
icon: "contact"
hidden: false
class: ""
tooltip: Clique para cirar um novo NPC nesta campanha
id: criarnovonpc
style: primary
actions:
  - type: templaterCreateNote
    templateFile: 5. Mecânicas/Templates/Novo NPC.md
    folderPath: 3. Campanhas/Eldoria RPG/4. NPCs
    fileName: ""
    openNote: false

```
```meta-bind-button
label: Criar Nova Localização
icon: "land-plot"
hidden: false
class: ""
tooltip: Clique para cirar uma Nova Localização
id: novolocal
style: default
actions:
  - type: templaterCreateNote
    templateFile: 5. Mecânicas/Templates/Nova Localização.md
    folderPath: 3. Campanhas/Eldoria RPG/5. Locais
    fileName: ""
    openNote: true
```
```meta-bind-button
label: Criar Novo Item
icon: "sword"
hidden: false
class: ""
tooltip: Clique para cirar um Novo Item
id: novoitem
style: primary
actions:
  - type: templaterCreateNote
    templateFile: 5. Mecânicas/Templates/Novo Item.md
    folderPath: 3. Campanhas/Eldoria RPG/6. Itens
    fileName: ""
    openNote: false
```
```meta-bind-button
label: Criar Novo Hex
icon: "hexagon"
hidden: false
class: ""
tooltip: Clique para cirar um Novo Hex
id: novohex
style: default
actions:
  - type: templaterCreateNote
    templateFile: 5. Mecânicas/Templates/Novo Hex.md
    folderPath: 3. Campanhas/Eldoria RPG/7. Hexcrawl
    fileName: ""
    openNote: false
```
