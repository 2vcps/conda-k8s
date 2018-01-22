# Help getting Conda and Jupyter Notebook running on Kubernetes

**Jupyterhub** is overkill for my use, but you may be interested in running it.

files included with this repo will help you use the base conda docker image with K8s.
In order of running:

nfs-pv.yaml - File with a persistent volume to map to your NFS device remember to use your IP and path, this path must be valid

nfs-pvc.yaml - Persistent Volume Claim so your Conda POD can attach the volume you created.

conda-pod.yaml - pod defination to start conda and install Jupyter, nb_conda(optional) and start jupyter notebook

conda-svc.yaml - Service file to start a Nodeport service to allow you to hit the jupyter server http interface.

flips_lots_of_flips.ipynb - File I was playing with for a data analytics class. Uses numpy to simulate coinflips 

README.md - this file, duh.


