IPython ontainerized and configured to run IPython Notebook server. Includes Numpy, Scipy, and Matplotlib libraries. 

To run the IPython Notebook without a password over HTTPS:

```
docker run -d -P johntfoster/ipython
```

To run the IPython Notebook with a password of your choosing over HTTPS:

```
docker run -d -P -e PASSWORD=$( read -p "Password: " -s PASSWORD && echo $PASSWORD ) johntfoster/ipython
```
