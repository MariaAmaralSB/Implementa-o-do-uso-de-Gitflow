Utilização do Gitflow para controle de versionamento dos projetos

# O que é Git?
 
Git é um sistema open-source de controle de versão. Com ele podemos criar todo histórico de alterações no código do nosso projeto e facilmente voltar para qualquer ponto para saber como código estava naquela data. Git também ajuda a controlar o fluxo de novas funcionalidades entre vários desenvolvedores no mesmo projeto com ferramentas para análise e resolução de conflitos quando o mesmo arquivo é editado por mais de uma pessoa em funcionalidades diferentes.

# O que é Gitflow

Gitflow é um framework criado para trabalhar em conjunto com o sistema de controle de versão do Git e ajuda a melhorar a organização de duas áreas: a gerencia de configuração e a gerencia de projetos.

# Repositórios Git

Um repositório nada mais é que uma pasta onde estão todos os arquivos do projeto, incluindo o versionamento. Os repositórios normalmente estão hospedados em algum lugar, como um servidor ou algum serviço de hospedagem, já que se trabalham em grupos que podem ir enviando suas alterações para o projeto e cada pessoa poderá fazer o download dessa alteração na sua máquina. Pelo fato do GIT ser um modo descentralizado de desenvolvimento, onde cada pessoa possui uma versão inteira do repsitório em sua máquina e só envia os pedaços que alterou para um local onde todo mundo pode fazer o download das alterações, sendo possivel até trabalhar sem internet e depois enviando o que trabalhou.

# Branches

As branches são as ramificações do projeto onde será feito o versionamento do projeto. O repositório central possui dois branches principais com vida infinita:
* master
* develop

O branch master é o branch principal, a HEAD do projeto, nele há somente as versões que estão em produção.

O branch develop possui todo o código já entregue e as últimas de desenvolvimento para a próxima versão. Quando o código do branch develop é considerado estável e pronto para ser implementado, todas as alterações devem ser mescladas de volta para o branch master e criada uma tag.

# Branches de suporte 

Junto aos branches master e develop utilizamos outros branches de suporte, para correção de erros, criação de melhorias e preparação para implementação. Ao contrário dos branches principais, esses tem uma vida limitada, uma vez que eles são removidas eventualmente. Os tipos de branches são :
* Branches de melhorias (features)
* Branches de lançamento (release)
* Branches de correções (hotfix)

Cada tipo de branch tem um próposito específico e segue regras de quais branches devem ser originadas e mescladas.
Branches de melhoria deve ser criado a partir do develop, deverá ser mesclado de volta para o develop.
A convensão de nome: qualquer nome exceto master, develop, release/, ou hotfix/.
Branches de melhorias são usados para desenvoler novas funcionalidades para o próximo release, ou descartado caso não seja útil ou seja um experimento.

# Branches de Release

Deve ser criada a partir do develop, deverá ser voltada para o master e o develop. Convensão de nome: release/2019.1
Branches de release são usadas para a preparação do próximo release de produção. Nessa branch não é permitida pequenas correções e atualizações de versões de arquivos. Na criação da branch de release é decidido qual versão o projeto terá, até este momento a branch develop reflete as alterações da próxima versão, independente de qual for. Esta decisão é feita na criação do branch de lançamento e segue as convensões de versionamento do projeto.

# Branches de correções 

Deve ser criado a partir do master, deverá ser voltada para develop e master. Convensão de nome: hotfix/ .Branches de correções são muito parecidos com branches de release em sua concepção, pois tem o mesmo objetivo de preparar uma versão para a produção, embora não planejada. Eles surgem da necessidade de agir imediatamente em uma versão de produção já implantada. Quando um bug crítico ocorre em uma versão de produção já implantada. Quando um bug crítico ocorre em produção um branch de correção precisa ser criado a partir da tag correspondente. A ideia é que o time que está trabalhando na próxima versão no branch develop possa continuar enquanto alguém prepara uma correção. 
