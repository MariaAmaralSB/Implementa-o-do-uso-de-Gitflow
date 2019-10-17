Utilização do Gitflow para controle de versionamento dos projetos

# O que é GIT?
 
Git é um sistema open-source de controle de versão. Com ele podemos criar todo histórico de alterações no código do nosso projeto e facilmente voltar para qualquer ponto para saber como código estava naquela data. Git também ajuda a controlar o fluxo de novas funcionalidades entre vários desenvolvedores no mesmo projeto com ferramentas para análise e resolução de conflitos quando o mesmo arquivo é editado por mais de uma pessoa em funcionalidades diferentes.

#Repositórios GIT

Um repositório nada mais é que uma pasta onde estão todos os arquivos do projeto, incluindo o versionamento. Os repositórios normalmente estão hospedados em algum lugar, como um servidor ou algum serviço de hospedagem, já que se trabalham em grupos que podem ir enviando suas alterações para o projeto e cada pessoa poderá fazer o download dessa alteração na sua máquina. Pelo fato do GIT ser um modo descentralizado de desenvolvimento, onde cada pessoa possui uma versão inteira do repsitório em sua máquina e só envia os pedaços que alterou para um local onde todo mundo pode fazer o download das alterações, sendo possivel até trabalhar sem internet e depois enviando o que trabalhou.

#Branches

As branches são as ramificações do projeto onde será feito o versionamento do projeto. O repositório central possui dois branches principais com vida infinita:
* Master
* develop
O branch master é o branch principal, a HEAD do projeto, nele há somente as versões que estão em produção.
O branch develop possui todo o código já entregue e as últimas de desenvolvimento para a próxima versão. Quando o código do branch develop é considerado estável e pronto para ser implementado, todas as alterações devem ser mescladas de volta para o branch master e criada uma tag.

#Branches de suporte 

Junto aos branches master e develop utilizamos outros branches de suporte, para correção de erros, criação de melhorias e preparação para implementação. Ao contrário dos branches principais, esses tem uma vida limitada, uma vez que eles são removidas eventualmente. Os tipos de branches são :
* Branches de melhorias (features)
* Branches de lançamento (release)
* Branches de correções (hotfix)
Cada tipo de branch tem um próposito específico e segue regras de quais branches devem ser originadas e mescladas.
