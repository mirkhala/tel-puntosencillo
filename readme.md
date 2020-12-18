# PoC Red Hat Process Automation Manager
_La PoC tiene como objetivo principal probar funcionalidades específicas de la plataforma **Red Hat Process Automation Manager**, aka: RHPAM sobre el proceso de **Punto Sencillo**._

## Punto Sencillo 📳

_Dada la necesidad de automatizar procesos que actualmente se realizan manualmente; se escoge el proceso **Punto Sencillo** como ejemplo de cómo la plataforma automatiza muchas actividades manuales._

Para más detalle en ![Business Process](https://github.com/mirkhala/tel-puntosencillo/tree/master/flow/puntoSencillopoceso.png?raw=true) puedes ver el diagrama.


### ¿Dónde probar el proceso? 🔧

_Una vez instalado **Red Hat Process Automation Manager** e importado el proyecto, ingresar al **kie-server** para probar el proceso bajo **/server/containers/{containerId}/processes/{processId}/instances**._

_**Ejemplo de URL del kie-server:**_

```
http://localhost:8080/kie-server/docs
```

### ¿Cómo probar el proceso? ✅

_Se prueban mediante un json especificando el container-id:: **puntoSencillo** process id: **puntoSencillo.PuntoSencilloBusinessProcess**:_

```
{
    "servicio": {
        "Servicio": {
            "esOnline": true,
            "esVigente": true,
            "equipo": "Cisco",
            "ms": "Internet",
            "ds": "Punto Sencillo",
            "ciudad": "Bogota",
            "direccion": "Cra. 58c #31-22",
            "esUnAlta": true,
            "banwidth": 50
        }
    }
}
```


Para más detalle en [resources](https://github.com/mirkhala/tel-puntosencillo/tree/master/resources) puedes ver el ejemplo.

## ¿Qué se espera? 🐪

_Se espera que una vez deje el archivo **file.csv** en el directorio **/tmp**, la ruta [Camel](https://github.com/mirkhala/tel-camel-csv2json)  transforme el archivo a **file.json** y dispare el proceso de **RHPAM**. El proceso mostrará el contenido del archivo inicial **file.csv** y se irán evaluando en diversos escenarios. Para más detalle ver: ._

[flow](https://github.com/mirkhala/tel-puntosencillo/tree/master/flow)

## Construido con 🛠️

_El proceso fue creado a manera de prueba, con distintos **Assets**. Para más información visita:_

* [Red Hat Process Automation Manager](https://access.redhat.com/documentation/en-us/red_hat_process_automation_manager/7.9/) - Automatización de procesos.

## Autores ✒️

_Los participantes de la PoC fueron:_

* **Jhon Salazar** - *Toma de Requisitos* - [jsalazar@redhat.com](jsalazat@redhat.com) - Account Solution Architect
* **Magda Martínez** - *Diseño de Proceso y Reglas de Negocio* - [magda.martinez@redhat.com](magda.martinez@redhat.com) - Specialist Solution Architect

## Agradecimientos Especiales 🎁
* **Rodrigo Ramalho** - *Integration* - [rramalho@redhat.com](rramalho@redhat.com) - Integration Specialist LATAM
* **Eduardo Rivas** - *Web Service* - [erivasza@redhat.com](erivasza@redhat.com) - Channel Solution Architect CEACA


---
⌨️ Creado por [Red Hat.](https://www.redhat.com/)