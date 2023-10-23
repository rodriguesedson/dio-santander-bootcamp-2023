# Dio Santander Bootcamp 2023
Java RESTful API - DIO Santander Bootcamp 2023
## Diagrama de classes
```mermaid
classDiagram
    class User {
        - name: string
        - account: Account
        - features: Features
        - card: Card
        - news: News
    }

    class Account {
        - number: string
        - agency: string
        - balance: float
        - limit: float
    }

    class Features {
        - icon: string
        - description: string
    }

    class Card {
        - number: string
        - limit: float
    }

    class News {
        - icon: string
        - description: string
    }

    User "1" *-- "1" Account
    User "1" *-- "n" Features
    User "1" *-- "1" Card
    User "1" *-- "n" News
