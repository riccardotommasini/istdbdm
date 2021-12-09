FROM jupyter/datascience-notebook

USER root

RUN apt-get update && \
	apt-get install -y graphviz && \
	apt-get clean && rm -rf var/lib/apt/lists/*

USER $NB_UID

COPY requirements.txt requirements.txt

RUN pip install -r requirements.txt

ENTRYPOINT ["jupyter","notebook","--NotebookApp.token=''"]