
Para mapear códigos é necessário primeiramentes criar nós com as palavras chaves. Lembrese de adicionar a tag element em cada palavra.
**alt + e** ![Texto alternativo](https://github.com/HamiltonVentura/MapperIdea-Java/blob/main/icones/element.png)


```mermaid
flowchart LR
    config --> mapperidea;
    mapperidea --> generators;
   
```
aṕos os **generators** pode se criar o nome dos geradores que o usuário esteja produzindo, exemṕlo:

```mermaid
    flowchart LR
        config --> mapperidea;
        mapperidea --> generators;
        generators --> JAVA;
        generators --> jsonServer;
        JAVA --> JasvaDomainModel;
        jsonServer --> dbJson;

style JAVA fill:#9f6,stroke:#333,stroke-width:2px;
```

