Vagrant Infrastructure Repository
============

Diese Projekt enthält alle Skripte um eine 

* eine Datascience-Umgebung mit Kafka, Spark und Jupyter Notebook aufzubauen
* eine CI/CD-Umgebung mit Jenkins und Docker aufzubauen

Vagrant wird genutzt um 

* 2 VMS für Kafka, Spark + Toree + Jupyter zu provisionieren
* 3 VMs für Jenkins, Docker Registry, Application Node zu provisionieren

Der Ordner "notebooks" enthält vorgefertigte Jupyter Notebooks.

Der Ordner "jenkins_jobs" enthält 2 fertige Jobs die entweder eine NodeJS oder eine Python Applikation deployen.

Der Ordner "jenkins_plugins" enthält die Plugins um die Jobs starten zu können (e.g. the Git-Plugin).

Der Order "scripts" enthält alle Shell-Skripte die zum Provisionieren benötigt werden.


Data Science
============

Run Kafka
-----------

```bash
vagrant up kafka
```

Run Spark + Jupyter
--------------

```bash
vagrant up datascience
```

Öffne "10.100.198.201:8888" im Browser um das Jupyter Notebook zu öffnen.

Das Beispiel kann zusammen mit "PyPoSim" als End-2-End-Szenario verwendet werden.
(https://github.com/crazzle/PyPoSim)


Continuous Delivery mit Docker
============

Run Jenkins
-----------

```bash
vagrant up jenkins
```

Run Docker Registry
--------------

```bash
vagrant up registry
```

Run Deployment Node
--------------

```bash
vagrant up node
```
