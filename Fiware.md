# FIWARE

Fiware es una plataforma de código abierto que proporciona un conjunto de componentes de software reutilizables para el desarrollo de soluciones de IoT y Smart Cities. Fue desarrollado por la Comisión Europea y un consorcio de empresas y organizaciones que trabajan en proyectos de ciudades inteligentes.

La plataforma Fiware se compone de varios módulos y herramientas que permiten a los desarrolladores construir aplicaciones y servicios de IoT de manera rápida y sencilla. Estos componentes están diseñados para ser modulares, interoperables y escalables, lo que significa que pueden integrarse fácilmente con otras tecnologías y soluciones existentes.

## Entre los componentes más destacados de Fiware se encuentran:

* Orion Context Broker: un sistema de gestión de datos que permite almacenar y acceder a información de sensores y dispositivos IoT en tiempo real.

* Cygnus: una herramienta que permite la integración de los datos de sensores y dispositivos IoT en sistemas de almacenamiento de datos.

* IDAS: un conjunto de protocolos y APIs que permiten a los dispositivos IoT conectarse a la plataforma Fiware y enviar datos.

* WireCloud: una plataforma de desarrollo de aplicaciones web que permite a los desarrolladores crear y desplegar aplicaciones de IoT y Smart Cities.

* Keyrock: un sistema de gestión de identidades y accesos que permite la autenticación y autorización de usuarios y dispositivos IoT en la plataforma.

## Orion Context Broker (OCB) 

* Administra la información de contexto, consultarla y actualizarla.

* Es como un intermediario entre entidades (Productores de contexto y consumidores de contexto).

* OCB implemente un API que se basa en el modelo NGSI(Registrar app de proveedores de contexto, actualizar información de contexto, ser notificado cuando surja cambios o consultar información).

Los servidores de OCB están escuchando en su puerto generalmente es el 1026 y utiliza la base de datos de MongoDB para almacenar el status actual de las entidades, no se almacena información histórica de cambios.

Principio fundamental de OCB es lograr la disociación total entre productores y consumidores de contexto. Ni los productores ni los consumidores saben quién es cada uno, solo interesa el evento.

Tola la comunicación entre los distintos componentes de OCB se realiza a través de API Restful NGSI v2. La información de contexto esta representada a través de elementos de contexto.

## Elementos de contexto

Es la información que es producida, recopilada y observada. Tienen asociado :

* Un EntityId y un EntityType único donde se identifica la entidad a la cual los datos de contexto hacen referencia.

* Atributos , son Triplas , contienen el Name, Type y el Value.

* Metadatos que contienen Atributos (Triplas), esto es opcional.

## Como interaccionar con la ApiRest NGSI v2

[Fiware-Training](https://fiware-training.readthedocs.io/es_MX/latest/ecosistemaFIWARE/ocb/)
