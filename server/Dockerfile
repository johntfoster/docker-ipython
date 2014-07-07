FROM johntfoster/ipython

MAINTAINER John Foster <johntfosterjr@gmail.com>


ADD notebook.conf /etc/supervisor/conf.d/notebook.conf
ADD start.sh /

EXPOSE 8888
CMD ["supervisord", "-n", "-c", "/etc/supervisor/supervisord.conf"]
