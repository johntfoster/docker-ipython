IPython containerized and configured to run IPython Notebook server. Inherits from johntfoster/ipython and adds support for LaTeX output in matplotlib.

To run the IPython Notebook without a password over HTTPS:

```
docker run -d -P johntfoster/ipython:latex
```

To run the IPython Notebook with a password of your choosing over HTTPS:

```
docker run -d -P -e PASSWORD=$( read -p "Password: " -s PASSWORD && echo $PASSWORD ) johntfoster/ipython:latex
```
