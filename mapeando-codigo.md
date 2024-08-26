# MAPEAMENTO DE CÓDIGOS.
Para mapear códigos é necessário primeiramentes criar nós com as palavras chaves. Lembrese de adicionar a tag element em cada palavra.
**alt + e** ![Texto alternativo](https://github.com/HamiltonVentura/MapperIdea-Java/blob/main/icones/element.png)


```mermaid
flowchart LR
    config --> mapperidea;
    mapperidea --> generators;
   
```
Aṕos os **generators** pode se criar o nome dos geradores que o usuário esteja produzindo, esses nomes dependenm de como o arquiteto/Analista decidir. obs. os nomes variaveis estão em verde.

```mermaid
    flowchart LR
        br.com.projeto --> config
        config --> mapperidea;
        mapperidea --> generators;
        generators --> JAVA;
        generators --> jsonServer;
        JAVA --> JavaDomainModel;
        jsonServer --> dbJson;

style JAVA fill:#9f6,stroke:#333,stroke-width:2px;
style jsonServer fill:#9f6,stroke:#333,stroke-width:2px;
style JavaDomainModel fill:#9f6,stroke:#333,stroke-width:2px;
style dbJson fill:#9f6,stroke:#333,stroke-width:2px;
```

COnhecer a estrutura de código é enssencial para mapear com eficiência.

## Estrutura e mapeamento (geradores)

### patterns
São os padrões, o código que será escrito literalemente.

 ```mermaid
flowchart LR
     JAVA --> domainModelJAVA;
     domainModelJAVA --> patterns;
     patterns --> padraoIncio;
     patterns --> padraoFim;
     padraoIncio --> B["{"];
     padraoFim --> F["}"];
style padraoIncio fill:#9f6,stroke:#333,stroke-width:2px;
style padraoFim fill:#9f6,stroke:#333,stroke-width:2px;
```

### start
São os padrões, o código que será escrito literalemente.

 ```mermaid
flowchart LR
     JAVA --> domainModelJAVA;
     domainModelJAVA --> patterns;
     patterns --> padraoIncio;
     patterns --> padraoFim;
     patterns --> start;
     padraoIncio --> B["{"];
     padraoFim --> F["}"];
     start --> match --> classes
     start --> body
     body --> write-pattern --> padrraoInicio;
style padraoIncio fill:#9f6,stroke:#333,stroke-width:2px;
style padraoFim fill:#9f6,stroke:#333,stroke-width:2px;
```

A princípio é facil gerar os códigos dessa forma, em um lado colocamos o código como deve ser escrito, no caso com o nó patterns, e em seguida adicionamos a sequencia no start denro do do body com a palara chave write pattern.

![image](https://github.com/user-attachments/assets/69d0eba0-890e-4ca5-abbf-2c7d957baea4)


