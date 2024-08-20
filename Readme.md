
# MapperIdea

# Índice

1. [Introdução](#introdução)
    1. [Pré-Requisitos](#Pré-Requisitos)
    2. [Principais conceitos](#Principais-conceitos-MaperIDea)
2. [Softwares Utilizados](#SOFTWARES-UTILIZADOS)
3. [Instalação e uso da ferramenta](#INSTALAÇÃO-E-USO-DA-FERRAMENTA)
4. [Construção de mapa](https://github.com/HamiltonVentura/MapperIdea-Java/blob/main/construcao.md)
5. [Referências](#referências)

7. 
## Introdução

MapperIdea é uma ferramenta que automatiza a geração de código em conjunto com o Freemind, uma ferramenta de mapas mentais. Usando MapperIdea, é possível converter mapas mentais em código, o que facilita o desenvolvimento de software e aproxima os stakeholders do projeto, tornando a colaboração mais eficiente e compreensível para todos os envolvidos.

### Mapperidea
__Finalidade da Ferramenta :__
Agilizar o desenvolvimento de Software com mapas mentais, possibilitando reaproveitamento de código através da arquitetura modelada pelo Desenvolvedor / Analista.
*Ideia : "Criar na unha  apenas uma vez"*


#### Pré-Requisitos
>[!IMPORTANT]
>**Para modeladores de regras de negócio** <br>
> Conceito de classes, atributos e propriedade <br>
> Os principais conceitos de Orientação a objetos <br>

#### Principais conceitos MaperIDea
>[!IMPORTANT]
>**Para programdores**<br>
> 1 - O **XML** é de extrema importância pois os documentos gerados pela Estrutura gerada são em mm que é um tipo de arquivo  Em sua base XML.<br>
> 2 - O **XPATH** Básico é essência para utilização do MI (MapperIdea) , através dele é possível correr os documentos XML. <br>
> 3 - O **XQUERY** facilita o entendimento da aplicação das funções dentro de Mapperidea.<br>
> 4 - **Orientação a Objetos** os principais conceitos.

## SOFTWARES UTILIZADOS 
- NODE 12 
- Freemind 1.0 + pacote de icones 

> O mapeamento é um processo em que os membros da equipe de desenvolvimento podem executar, envolve "copiar" o codigo traduzindo-o em mapas mentais, 
> os quais poderão se alterados atualizados uma vez montados, sem necessidade de alterar código "na unha".

Após efetuar os mapeamentos, é necessário executar via linha de comando a geração de códigos, que é uma conversão do codigo mapeado em codigos práticos.
A baixo é uma ilustração de como é o processo de criação dos mapas.

```mermaid
flowchart LR
    Gerar-mapa --> Arquitetura
    Gerar-mapa ---> Regra-de-negocio;
    Regra-de-negocio --> Mapas-Mentais-Freemind;
    Mapas-Mentais-Freemind --> Classes-atributos;
    Mapas-Mentais-Freemind --> funções;
    Mapas-Mentais-Freemind --> pacotes;
    Arquitetura --->PHP;
    Arquitetura --->JAVA;
    Arquitetura --->Html;
    Arquitetura --->JAVASCRIPT;     
```
O fluxo de utilização dos mapas mentais funciona da seguinte forma, O Mapperidea utiliza o código gerado pelos mapas mentais, sobe para o servidor essas informações, e como retorno ele traz o código escrito na arquitetura escolhida que foi construida.

```mermaid
flowchart LR
    sobe-mapa-regras-de-negócio --> servidor;
    sobe-mapa-da-arquitetura --> servidor;
    servidor --> retorna-código-escrito;   
```
A idéia principal é após mapeamento do código da arquitetura, alterar apenas os mapas mentais de regra de negócio, automatizando assim os processos referentes a codificação do sistema em construção ou alteração.



## INSTALAÇÃO E USO DA FERRAMENTA
#### Instalar antes o node versão 14
  **Para Linux**
~~~bash
sudo apt install npm
~~~
**para Windows**
~~~bash
choco install nodejs-lts --version=14.17.6
~~~

~~~bash
npm install mapperidea-cli -g
~~~

- teste usando o comando 

~~~bash
mi -h
~~~

 - Na sequência utilize  com os dados fornecidos pela Mapperidea para autorizar seus acessos.
```authorize|a <email> <machine> <server>```


### Observações: ###

- inicialize o projeto com o nome do projeto e o nome do arquivo

mi init <nome do projeto> <arquivo.mm>
Atualize o projeto subindo as informações para o servidor
mi push <nome do projeto>
O fluxo repetitivo do projeto é sempre alterar o arquivo, dar um push no servidor para atualização, e então utilizar o comando para geração de código.



### ICONOGRAFIA ####
Para adicionar um ícone a qualquer um de seus nós em seu mapa mental utilize a tecla de atalho "Alt + I" o qual abrirá uma tela de icones, você poderá clicar no ícone desejado ou poderá utilizar as teclas de talhos. Acompanhe a baixo os ícones mais utilizados para mapeamentos de regra de negócio.<br>
<img src="https://github.com/HamiltonVentura/MapperIdea-Java/blob/main/icones/telaIcones.png" alt="Imagem telas de ícones" width="200">


## Package
![Texto alternativo](https://github.com/HamiltonVentura/MapperIdea-Java/blob/main/icones/Package.png)
O ícone Package, siginifica pacote, indica diretórios. Todas as vezes que existir esse icone nos mapas mentais significa que existe um diretório, isso ajuda a organizar
e melhorar o entendimento do código.Pela padonização das teclas utilize **A tecla p**


## Direct-to-Field
![Texto alternativo](https://github.com/HamiltonVentura/MapperIdea-Java/blob/main/icones/Mapping.directToField.png)
O icone **Direct to Field**, representa o campo de entrada de dados, por exempo: A Classe Vendedor possúi nome, e sobrenome, logo nome e sobrenome apresentarão esses icones de **Direct To Field**, quando no sistema vocês adicionarem esse campo será necessário na Arquitetura do software, identificar o icone e então executar alguma ação, como por exemplo criar um campo input. **Utilize a tecla D**

## Icon-Descriptor-Class
![Texto alternativo](https://github.com/HamiltonVentura/MapperIdea-Java/blob/main/icones/Descriptor.class.png)
Ícone de descrição de classe, em seu nó adicione esse ícone para indicar que é uma classe comum. Tecla de talho **alt+c**

## Icon-Descriptor-Bean
![Texto alternativo](https://github.com/HamiltonVentura/MapperIdea-Java/blob/main/icones/Descriptor.bean.png)
Ícone de descrição de classe Bean, em seu nó adicione esse ícone para indicar que é uma classe do tipo Bean. Tecla de atalho **alt+b**

## Icon-One-to-Many
![Texto alternativo](https://github.com/HamiltonVentura/MapperIdea-Java/blob/main/icones/Mapping.oneToMany.png)
Uma determinada classe pode ter subclasses, inferindo a relação "Um parar muitos", um exemplo simples seria 
uma classe "Orçamento" que contem diversos itens/produtos. como tecla de atalho utilize **alt+o**

## Icon-Many-to-one
![Texto alternativo](https://github.com/HamiltonVentura/MapperIdea-Java/blob/main/icones/Mapping.manyToOne.png)
Uma determinada classe pode ser o item de uma classe pai, para isso utilizamos icone Muitos para um.**alt+d**

## Icon one-to-one
![Texto alternativo](https://github.com/HamiltonVentura/MapperIdea-Java/blob/main/icones/Mapping.oneToOne.png)
O ícone one-to-one indica que existe a relação um para um. Por exemplo classe Empregado possui vinculo com um computador, assim sendo, não possuiria vinculos com mais computadores estabelecendo a relação um para um. Tecla de atalho **alt+r**

## Icon element
![Texto alternativo](https://github.com/HamiltonVentura/MapperIdea-Java/blob/main/icones/element.png)
O ícone element é utilizado para diversas indicações, mas principalmente com palavras chaves do Mapperidea e em momentos como descritivos de algumas funcionalidade. **alt+e**

[Construção de mapa simples](/construcao.md)




