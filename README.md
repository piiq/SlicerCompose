# Slicer Compose

Docker-compose implementations for running 3D Slicer in cloud environments.

## Project structure

```
.
├── Slicer      <- Slicer app container
└── docs        <- Documentation and images
```

## Create a new VM

As an example GCE is used as the cloud provider.

Instructions of setting up a new machine are pretty basic. They go through installing basic packages, git and docker engine.

[See detailed walkthrough here](docs/gceconfig.md)

By the time you are done you should have a running machine and you are connected to the machine via ssh.

## Clone the SlicerCompose repository

```bash
git clone git@github.com:piiq/SlicerCompose.git
```


