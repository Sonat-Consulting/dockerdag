#Fagdag: Docker 101

********************************************
##Ting du trenger(gjerne før fagdagen):
1. OSX/Windows: Last ned docker-toolbox på https://www.docker.com/docker-toolbox (docker, docker-compose, virtualbox)
2. Installer node.. https://nodejs.org/en/download/

********************************************

##Oppgaver:

Last ned kode: 
		git clone https://github.com/Sonat-Consulting/dockerdag.git

Opprett en dockermaskin:

		docker-machine create --driver virtualbox myDocker
		docker-machine env myDocker
		eval $(docker-machine env myDocker)

Kjør ```docker-machine ip``` og se ipadressen!

### Oppgaver 1:
#####Bli kjent med docker: Opprett en dockerfil, bygg et dockerimage og start en container.

Det er på forhånd laget 3 webapplikasjoner, dockerifiser så mange av de du kan.
Alle har en løsningsmappe, dette er dockerfile som kan brukes i oppgave 2 dersom oppgave 1 gikk te h.... IKKE JUKSE!!! :)

Spør om hjelp hvis en sitter fast.

1. Springboot   (Java)

		cd springboot
		mvn install
		java -jar target/springboot-1.0-SNAPSHOT.jar
		curl mot localhost:8081/ping  (eller bruk browser)


2. NodeDock     (Node)

		cd nodeDock
		npm install
		node nodeapp.js
		curl localhost:8082/ping (eller bruk browser)

3. SimpleNancy  (.NET , denne e litt avansert og mest med som showcase)

        cd SimpleNancy
        xbuild SimpleNancy.sln
        mono ./SimpleNancy.SelfHost/bin/Debug/SimpleNancy.SelfHost.exe
		curl localhost:8082/ping (eller bruk browser)


Alle web applikasjoner har en løsningsmappe. Dette er til bruk i steg 2 hvis du ikke fikk til denne oppgaven. Spør om hjelp hvis en sitter fast.


###Oppgave 2
##### Bli kjent med docker-compose: Få servicer til å prate sammen! Java --> Node --> MongoDB eller .NET --> Node --> MongoDB

		Gå til dockerdag, og se på docker-compose.yml
		docker-compose up
		curl localhost:8081/count  / eller bruk browser

Prøv å ferdigstill docker-compose.yml!

(PS. Bruk gjerne dockerfile i løsningsfolder i de respektive java/net/node i denne oppgaven)


###Oppgave 3
##### Utforsk, lek og tafs på Docker

* Har du noe eget prosjekt du vil prøve å dockerifisere?
* Lyst å prøve å hive containeren din ut i en cloud?
* Utforske docker sitt REST API?
* Lyst å leke med Docker Swarm?
* Utforske docker hub?
* Sette opp Continues Delivery med Docker?
* Utforske andre alternative container teknologier ([lxd](http://www.ubuntu.com/cloud/lxd), [rkt](https://github.com/coreos/rkt), andre?)?
* Play with docker! 

Vi avslutter dagen med at alle grupper fremlegger hva de har jobbet med, og hvordan det gikk. Tenk også på følgende spørsmål for diskusjon:

* Hva er lett? Hva er vanskelig?
* Utfordringer?
* Vil du anbefale Docker til kunden?
* Etter din mening: Når bruke Docker og når IKKE bruker Docker?


