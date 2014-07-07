FROM johntfoster/ipython

MAINTAINER John Foster <johntfosterjr@gmail.com>

ENV HOME /root

RUN apt-get update
RUN apt-get -yq install texlive
RUN /usr/bin/yes | pip uninstall matplotlib
RUN pip install matplotlib

ADD notebook.conf /etc/supervisor/conf.d/notebook.conf
ADD start.sh /

RUN ipython profile create
RUN echo "c.FileNotebookManager.notebook_dir = u'/ipy'" >> /root/.ipython/profile_default/ipython_notebook_config.py

RUN mkdir -p /ipy
VOLUME ["/ipy"]

EXPOSE 8888
CMD ["supervisord", "-n", "-c", "/etc/supervisor/supervisord.conf"]
