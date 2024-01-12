# Welcome to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml            # The configuration file.
    docs/                 # The folder in with all the docs live
        index.md          # The documentation homepage.
        ...               # Other markdown pages, images and other files.
        subfolder         # Creates a navigation
            some-topic.md # Creates a page with the name 'some topic'

## Material for MkDocs
To have a better theme and quite some nice features we use [Material for MkDoks](https://squidfunk.github.io/mkdocs-material/)

Here is a list of [already included plugins](https://squidfunk.github.io/mkdocs-material/plugins/)

Here are some example [extensions that we could activate](https://squidfunk.github.io/mkdocs-material/reference/admonitions/)


## Here have some mermaid diagrams

The documentation can be found here [Mermaid Diagrams](https://mermaid.js.org/intro/)

### Flowcharts
```mermaid
flowchart LR
  subgraph TOP
    direction TB
    subgraph SomeOtherSubGraph
        direction RL
        i1 -->f1
    end
    subgraph SomeSubGraph
        direction BT
        A[Start] --> B{Is it?}
        B -- Yes --> C[OK]
        C --> D[Rethink]
        D --> B
        B -- No ----> E[End]
    end
  end
  A --> TOP --> B
  SomeOtherSubGraph --> SomeSubGraph
```

### Sequence diagram
```mermaid
sequenceDiagram
    Alice->>John: Hello John, how are you?
    John-->>Alice: Great!
    Alice-)John: See you later!
```

### Class diagram
```mermaid
---
title: Animal example
---
classDiagram
    note "From Duck till Zebra"
    Animal <|-- Duck
    note for Duck "can fly\ncan swim\ncan dive\ncan help in debugging"
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
        +String beakColor
        +swim()
        +quack()
    }
    class Fish{
        -int sizeInFeet
        -canEat()
    }
    class Zebra{
        +bool is_wild
        +run()
    }
```

### State diagrams
```mermaid
stateDiagram
    [*] --> Still
    Still --> [*]

    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
```

### ER-Diagrams
```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```

### Gantt
```mermaid
gantt
    title A Gantt Diagram
    dateFormat YYYY-MM-DD
    section Section
        A task          :a1, 2014-01-01, 30d
        Another task    :after a1, 5d
    section Another
        Task in Another :2014-01-12, 12d
        another task    :10d
```

### Git Graph
```mermaid
---
title: Example Git diagram
---
gitGraph
   commit
   commit
   branch develop
   checkout develop
   commit

   commit
   checkout main
   merge develop
   commit
   commit
```

### User Journey
```mermaid
journey
    title My working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 5: Me
      Sit down: 5: Me
```