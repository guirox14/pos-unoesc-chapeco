
------ INICIO do artigo ------ 
####Universidade do Oeste de Santa Catarina – Unoesc
####Pós-Graduação em Desenvolvimento Web, Cloud e Dispositivos Móveis - WebMob
####Disciplina: HTML5+CSS3
####Professor: Jean Carlo Nascimento
####Acadêmico: Guilherme Mendes Senger
###Atomic Design
#####Resumo
O uso de softwares vêm crescendo assustadoramente ano após ano, e com isso cresce a demanda por desenvolvimento ágil e num curto espaço de tempo. Sendo essa uma necessidade a cada dia maior, uma das técnicas que vem ganhando espaço é chamada de Atomic Design, que apresenta a proposta de átomos, moléculas, organismos, templates e páginas. Essa técnica propõe um reuso dos componentes, a fim de ganhar tempo quando é necessário efetuar alguma mudança na interface, pois propõe que a alteração seja feita apenas num único local. Este artigo aborda um resumo da técnica do design atômico, bem como etapas, vantagens, conceitos e exemplos de seu uso.
#####1) O que é?
O Atomic Design ou Design Atômico, em português, é uma criação do webdesigner Brad Frost, que se baseou nas aulas de química para explicar como os componentes de uma página interagem. Segundo ele, as páginas são sistemas formados por elementos simples que, quando integrados, podem criar sistemas complexos, mas organizados, da mesma forma que átomos se ligam para criar moléculas e organismos na natureza.
#####2) Como funciona
Consiste em dividir o sistema em cinco partes, conforme descritas abaixo:</br></br>
**2.1 Átomos**: são as partes mínimas de cada página, mas que sozinhas não são úteis. Exemplos: inputs, buttons, labels de formulários, etc.</br></br>
**2.2 Moléculas**:Juntando um ou mais átomos, cria-se uma molécula, que faz com que os átomos funcionem com um objetivo único, criando um componente mais concreto. Por exemplo, um label, uma caixa de texto e um botão podem formar um componente de pesquisa.
**2.3 Organismos**: São grupos de moléculas, que formam partes maiores (ou sessões) de uma página. Norteiam a navegação de leitura do conteúdo da interface. A criação de organismos torna possível o reuso de componentes, pois um organismo pode ter moléculas de vários tipos diferentes.</br></br>
**2.4 Templates **: Nesta etapa diversos organismos são acoplados para se criar um modelo vivo, ou seja, o esqueleto de uma página HTML funcional, mas de baixa fidelidade (wireframes). Neste momento, já é possível validar o layout com o cliente, pois foi produzido algo concreto, do ponto de vista dele.
**2.5 Páginas**:Adicionando-se conteúdo a um template, tem-se uma página, com cores, tipografia, imagens e vídeos, facilitando a validação do template e identificação de ajustes necessários, culminando no produto final.





#####3) Para que usar
Facilitar a criação de layouts através do uso modular e progressivo de componentes dinâmicos, aumentando a rapidez e produtividade dos designer e desenvolvedores, pela facilidade de experimentação, alterando a combinação dos elementos para criação de novas estruturas.
Agilidade na alteração de componentes: como é baseado em componentes, qualquer alteração pode ser feita uma única vez e todos os templates que usam esse componente já estarão alterados.
Centralização de informações: ao utilizar o Pattern Lab, o time de desenvolvimento tem em mãos uma biblioteca centralizada com informações de cada componente. Isso torna fácil o acesso às funcionalidades.
No lugar de apresentar para o cliente modelos estáticos, é possível criar desde o início um protótipo responsivo, que poderá ser testado e evoluído diretamente nos dispositivos que irão executá-lo.
#####4) Onde usar?
Em projetos de médio a grande porte. Não faz sentido criar toda uma biblioteca (Pattern Lab) centralizada de componentes se o projeto tiver apenas um ou dois templates. A técnica do design atômico mostra seu propósito quando existem vários componentes que serão usados em uma grande quantidade de templates e páginas.
Vale destacar que o time precisa ter bastante confiança entre si, pois nem tudo será documentado. Por exemplo: o componente que monta um *header* na página inicial será o mesmo para as demais páginas, não sendo necessário documentar cada parte do *header* em cada template de página.
#####5) Exemplos:
Seguem abaixo exemplos de cada etapa do atomic design aplicado num site real das [Ferramentas Gerais] (http://www.fg.com.br).
#####5.1 Átomos
Tags htmls que por si só não úteis, pois não existe vínculo entre elas.</br>
<img src="https://cloud.githubusercontent.com/assets/15130723/10555517/bab47aec-7446-11e5-8a0c-b9a3ba5877db.png" alt="atoms" title="Atoms"/></br>
#####5.2 Moléculas
Os átomos do item anterior foram agrupados, criando uma estrutura com possível utilidade para quem está usando.</br>
<img src="https://cloud.githubusercontent.com/assets/15130723/10555518/babaab74-7446-11e5-824f-aed4ffbb3e6e.png" alt="molecules" title="Molecules"/></br>
#####5.3 Organismos
Foi criado um novo componente a partir da junção da molécula do item anterior, somada a outras moléculas já criadas.</br>
<img src="https://cloud.githubusercontent.com/assets/15130723/10566802/7e736888-75cf-11e5-8e46-4116e9501175.png" alt="organisms" title="Organisms"/></br>
#####5.4 Templates
Foi aplicado o organismo do item anterior num wireframe, dando forma à página inicial do site.</br>
<img src="https://cloud.githubusercontent.com/assets/15130723/10555515/baa9c5ac-7446-11e5-9eac-aadf05215071.png" alt="templates" title="Templates"/></br>
#####5.5 Pages
Por fim, foi criada a página real, utilizando os átomos, moléculas, organismos e o template dos itens anteriores.</br>
Esta é a página que será entregue ao cliente para posterior avaliação/testes.</br>
<img src="https://cloud.githubusercontent.com/assets/15130723/10555516/baafe8f6-7446-11e5-9731-10cb8bd39f16.png" alt="pages" title="Pages"/></br>
#####6) Referências
[http://pt.slideshare.net/bradfrostweb/atomic-design](http://pt.slideshare.net/bradfrostweb/atomic-design)</br>
[http://bradfrost.com/blog/post/atomic-web-design/](http://bradfrost.com/blog/post/atomic-web-design/)</br>
[http://nomadev.com.br/atomic-design-por-que-usar/](http://nomadev.com.br/atomic-design-por-que-usar/)</br>
[http://nomadev.com.br/atomic-design-com-angularjs/](http://nomadev.com.br/atomic-design-com-angularjs/)</br>
[http://tableless.com.br/o-que-e-design-atomic/] (http://tableless.com.br/o-que-e-design-atomic/)</br>
[http://patternlab.io/] (http://patternlab.io/)</br>
[http://www.frontendbrasil.com.br/tutoriais/atomic-design-como-funciona/] (http://www.frontendbrasil.com.br/tutoriais/atomic-design-como-funciona/)</br>
[http://arquiteturadeinformacao.com/mobile/atomic-design-redesenhando-os-entregaveis-de-designers-e-desenvolvedores/] (http://arquiteturadeinformacao.com/mobile/atomic-design-redesenhando-os-entregaveis-de-designers-e-desenvolvedores/)</br>

------ FIM do artigo ------
