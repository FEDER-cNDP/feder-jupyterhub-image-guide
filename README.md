# FEDER JupyterHub: Pre-Built Images

When you start a server on the FEDER JupyterHub, you choose one of these images.

## Minimal Starter Jupyter Lab
A general-purpose JupyterLab environment. Use it for everyday notebooks and
analysis.

## Argus FEDER
JupyterLab with the ARGUS agent, TokSearch, and the DIII-D data stack
pre-installed. It's selected automatically when you work in a FEDER CollabStudio.
The spawn page always shows the current version.

### First-time setup (once per user)
Your settings are kept in persistent storage, so you only do this once.

1. Get your NRP LLM API key.
2. Open a Terminal in JupyterLab and run:

       echo 'NRP_API_KEY=<your key>' >> ~/work/_User-Persistent-Storage_CephBlock_/.env
       chmod 600 ~/work/_User-Persistent-Storage_CephBlock_/.env

3. In a notebook, run `%fdp_login` and approve the link it prints.

### Save your work
Only `/home/jovyan/work/_User-Persistent-Storage_CephBlock_` survives a server
restart. Anything saved elsewhere is lost when the server stops.

### More about Argus FEDER
- [Project README](https://github.com/FEDER-cNDP/feder-argus)
- [What's in the image](https://github.com/FEDER-cNDP/feder-argus/blob/main/image/README.md)
- [Changelog](https://github.com/FEDER-cNDP/feder-argus/blob/main/CHANGELOG.md)
- [All versions](https://github.com/FEDER-cNDP/feder-argus/tags)
