# dockerPruebas
```
FROM debian:latest
RUN apt-get update &&\
	apt-get install -y nodejs npm git &&\
	apt-get clean &&\
	git clone https://github.com/MatiasVilche/dockerPruebas.git &&\
	cd dockerPruebas && npm i
EXPOSE 3000

ENTRYPOINT ["node", "dockerPruebas/index.js"]
