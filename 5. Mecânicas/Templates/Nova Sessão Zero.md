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

## Tema central da campanha

Resuma em uma frase o que define e move sua campanha.

- [ ] Apresente o tema da aventura. É uma investigação? Focada em combate? Adentrar nas profundezas de masmorras? Focado em interação social? Deixe os jogadores cientes do que estão se metendo.

## Seis verdades sobre a campanha

Quais são as seis coisas mais importantes que você deseja que seus jogadores entendam sobre o mundo e a campanha?

- [ ] Reforce a motivação principal dos personagens para que consigam aproveitar a aventura ("Seus personagens trabalham juntos em cooperação para proteger os cidadãos da Cidade das Arcadas").


## Patronos e Facções

Quem são os patronos e facções dos quais os personagens podem fazer parte? O que une os personagens para a aventura nesta campanha?

## Vilões

Quem ou quais são os três principais impulsionadores desta campanha? |Geralmente, esses são vilões. *Você não quer compartilhar isso com seus jogadores.* Em vez disso, crie uma ficha para cada vilão, associando-o a uma facção. Use os objetivos das facções. 

## Opções de personagem e regras da casa

Quais são as especificidades da criação de personagens para este mundo? Quais são os limites de construção de caráter neste mundo? Quais regras da casa estão em jogo?


## Limites e Ferramentas de Segurança

Discuta quais ferramentas de segurança você e seus jogadores se sentem confortáveis em usar durante esta campanha. Discuta todos os tópicos delicados a serem evitados. Consulte este guia sobre [Como fazer uma Sessão 0](https://youtu.be/NgdVNoKkCzc) para obter detalhes.

- [ ] Descreva quais sessão as ferramentas de segurança usadas
    - [ ] **Limites:** Personagens fazendo tortura, atividades sexuais sem consentimento ou assédio, conflito não-consensual entre o grupo, abuso de animais, sexismo ou misoginia, qualquer sentimento ou discurso anti-LGBT
    - [ ] **Véu:** Racismo, tortura, atividades sexuais consensuais.
    - [ ] “Vamos dar uma pausa”

## Inspirações para a Campanha

Que livros, obras de arte, música, filmes e programas de TV inspiram sua campanha? Compartilhe-os com seus jogadores e use-os você mesmo quando precisar de inspiração.