# deoldify-podman

This repo contains 2 ContainerFiles to build the deoldify image and video colorization code in a podman container.

The ```ContainerFile`` file is the one that should be used if you have a GPU.  If not, use the ```ContainerFile-CPU`` file.

Both ContainerFiles use the Fedora35-Python3 container image as the base image.

**Instructions for building:**

```podman build  --layers=false -f ContainerFile -t deoldify .```

**To start the container:**

```podman run -d --name deoldify -p 8888:8888 -p 5000:5000 deoldify```

**Running The Jupyter Notebook**

Access the Jupyter Lab interface by browsing to ```http://localhost:8888```

Once you are in that interface, choose either image colorizer (```ImageColorizer.ipynb```) or video colorizer (```VideoColorizer.ipynb```) and follw the instructions/run the code in the selected notebook.

Huge shouout jantic (Jason Antic) the Creator of DeOldify as well as Nicholas Renotte, whose YouTube vide got me interested in the project.
