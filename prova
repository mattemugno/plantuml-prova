@startuml
actor Utente
participant "Frontend" as FE
participant "Backend API" as BE
database "Database" as DB

Utente -> FE: Inserisce credenziali
FE -> BE: POST /login
BE -> DB: Verifica utente
DB --> BE: Dati utente

alt Credenziali valide
    BE --> FE: 200 OK + token
    FE --> Utente: Login effettuato
else Credenziali non valide
    BE --> FE: 401 Unauthorized
    FE --> Utente: Mostra errore
end

@enduml
