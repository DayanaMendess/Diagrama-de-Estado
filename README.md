# Diagrama-de-Estado


@startuml

[*] --> Disponible

state Disponible {
    [*] --> Esperando_Reserva
    Esperando_Reserva --> Reservado : Reservar_Asiento
}

state Reservado {
    Reservado --> Disponible: Cancelar_Reserva
    Reservado --> Cancelado : Cancelar_Vuelo
}

state Cancelado {
    Cancelado --> Disponible : Vuelo_Disponible
}

    
@endum1

