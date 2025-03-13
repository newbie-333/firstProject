#README
***********************************************************************************************************
                                    SISTEMA DE GESTION DE RESERVAS
***********************************************************************************************************
// Aquí empieza mi carrera. //

* Motivación: Trabajo en un restaurante donde se cogen las reservas por llamada, quiero arreglar eso.
* Formato: WebApp
* Herramientas: ** Backend: Springboot, 
                ** DATABASE: MySQL (workbench)
                ** Frontend: Angular
                ** JAR/ HIBERNATE: interactuar con la base de datos (POR DECIDIR)
                ** Esquemas: Obsidian

* 1r Paso: Definir el sistema (Esquema obsidian)

    SISTEMA DE GESTIÓN DE RESERVAS: REQUIRIMIENTOS 
            * Sistema de reservas que permite al usuario reservar una mesa en una fecha y hora 
            concretas y al administrador gestionar las reservas.

            1. Usuarios:
                * Pueden registrarse e iniciar sesión
                * Pueden ver la disponibilidad de las citas
                * Pueden hacer una reserva
                * Pueden ver, cancelar y editar reservas
            
            2. Administradores:
                * Pueden ver todas las reservas.
                * Pueden añadir, editar o eliminar mesas.
                * Pueden gestionar la disponibilidad de las mesas.
                * Pueden gestionar usuarios.

            3. Funcionalidades adicionales: 
                * Confirmación por correo electrónico 
                * Pantalla de gestión para los administradores con una interfaz adecuada 
                  para la gestión de reservas
                * Base de datos segura y escalable
    
    BASES DE DATOS (MYSQL): 

            1. Definir datos:
                * Clientes (id_cliente (PK), nombre, teléfono, correo electrónico, dirección, fecha de registro)
                    ** Un cliente puede hacer varias reservas
                    ** Una mesa puede ser reservada varias veces pero solo una a la vez 
                    ** Una mesa esta asociada a un cliente y a una mesa
                    ** Un administrador gestiona las reservas

                * Reservas (id_reserva(PK), fecha y hora, num_mesa, id_cliente, estado de la reserva(booleano confirmada))
                * Mesa (num_mesa(PK), capacidad, ubicacion(terraza,interior), estado)
                * Administradores (id_trabajador, nombre, puesto)
                * Pago para confirmar (id_pago(PK), id_reserva, cantidad,estado_pago)

                * Relaciones:
                    ** Cliente-Reserva: de 1 a muchos, puede hacer varias reservas
                    ** Mesa-Reserva: de 1 a muchos, puede tener varias reservas a lo largo del tiempo
                    ** Reserva-Cliente: de muchos a 1, una reserva esta asociada a un cliente
                    ** Reserva-Pago: 1 a 1, una reserva puede tener un pago asociado
                    ** Reserva-Mesa: de muchos a 1, cada reserva esta asociada a una mesa


            2. Crear diagrama Entidad relació: 
                 
                 * Primer diagrama E-R (Básico y de partida)
                 
                



