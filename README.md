# 3. Desarrollo de la propuesta
En este capítulo se describe la justificación e implementación de las tecnologías utilizadas en cada una de las fases para el desarrollo del sistema moderno basado en la arquitectura de microservicios, la integración entre el nuevo sistema y el sistema heredado (ERP) y finalmente el prototipo móvil para evaluar el esquema arquitectónico que representa la parte del cliente.
## 3.1. Justificación de tecnologías
En esta sección se explica la razón de las tecnologías empleadas para el desarrollo de un sistema basado en microservicios por tal motivo solo se hace mención breve de las tecnologías sin entrar a profundidad en cada una de ellas. Para el desarrollo del nuevo sistema se ha optado por el uso de Spring Boot junto con Spring cloud.
### Spring Boot Framework:
Spring boot es un proyecto de código abierto basado en Spring Framework, utilizado para el desarrollo de microservicios gracias a la configuración automática de dependencias por medio de anotaciones, esto permite a los desarrolladores centrarse en la lógica de la aplicación sin preocuparse por la configuración de dependencias.

Las características más sobresalientes del Spring Boot son:

* Configuración automática inteligente.
* No es necesario implementar archivos WAR gracias a su servidor web incorporado Tomcat
* Facilita la gestión de dependencias.

### Spring Cloud
Spring Cloud es una colección de herramientas que proporciona soluciones a algunos de los parones más comunes al construir sistemas distribuidos, junto con Netflix OSS lograron asbtraer diversos patrones como:

* API Gateway:Zuul Gateway
* Service Registry: Eureka Server
* Circuit Breaker: Hystrix 
* Load Balancer: Ribbon 
* Distribuited Tracing: Zipkin y Sleuth
* Externalized Configuration: Config Server
* Rest Client: Feign

Para entender como se emplean todas las tecnologías mencionadas se presenta el siguiente esquema arquitectónico para la construcción de microservicios con Spring Boot y Spring Cloud, Zuul Gateway proporciona un punto de entrada al ecosistema de microservicios, lo que proporciona capacidades de enrutamiento dinámico, Discovery Server permite registrar todos los microservicios y sus diferentes instancias, Load Balancer proporciona equilibrio de carga del lado del cliente en llamadas a otros microservicio, Distributed Tracing permite monitorizar el tiempo total de una traza desde que el cliente realiza una petición hasta que recibe una repuesta y Config Server configuración externa para todos los microservicios.

![Microservices](https://github.com/Practicum42-MP-20201/actividad5-apartadodesarrollo-CristianGaona/blob/master/Images/ARMS.png)
