## GEN CLI

Para que una mesa pueda crear los jobs y pipelines, es ***mandatorio*** actualizar o instalar la ultima versión (1.9) del microservico de jenkins el cual indica el lineamiento del GEN CLI.

```
pip3 install jenkins-microservice===1.9 --trusted-host devops-gns-eastus2.cloudapp.azure.com
```

---

Por ejemplo:

```
gencli create -f visor/Backend -type BACKEND -t visor -p ms-cn-visor-omnicanal-arbol -g https://github.com/Visor-TdP/ms-cn-visor-omnicanal-arbol.git 
```

La versión 1.9 genera una carpeta en cada ambiente:
 * Visor_dev
 * Visor_cert
 * Visor_prod

Por el momento, el combo para escoger el ambiente todavía enseña los 3 ambientes:
 * dev
 * cert
 * prod

Solo se debe escoger el ambiente correspondiendo a la carpeta.  Esta ambiguidad se va a corregir en la próxima versión.

Opción ***-type*** nos deja escojer el tipo de proyecto (en el caso de Backend):

<style type="text/css" rel="stylesheet">
	table {
		border-collapse: collapse !important;
	}
	th {
		border: 2px solid black !important;
		background-color: #d3d3d3;
	}
	td {
		border: 2px solid black !important;
	}
	hr {
		border: 2px solid black !important;
	}
</style>

|*Tipo*           |*Descripción*                         |
|:---             |:---                                  |
|***BACKEND***    |microservicios desarrollados con `mvn`|
|***BACKEND_LIB***|librerias de Backend                  |

***ojo*** - no confundir el tipo que va a causar un error!

<table border="2">
	<tr><th border>Tipo</th><th>Descripción</th></tr>
	<tr><td border>BACKEND</td><td>microservicios desarrollados con `mvn`</td></tr>
	<tr><td border>BACKEND_LIB</td><td>librerias de Backend</td></tr>
</table>
