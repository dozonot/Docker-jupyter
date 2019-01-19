FROM jupyter/minimal-notebook:latest

USER $NB_USER

RUN pip install jupyter_contrib_nbextensions && \
    jupyter contrib nbextension install --user && \
    git clone https://github.com/lambdalisue/jupyter-vim-binding /home/jovyan/.local/share/jupyter/nbextensions/vim_binding && \
    pip install sympy numpy pandas matplotlib networkx scipy && \
    jupyter nbextension enable vim_binding/vim_binding

COPY jupyter_notebook_config.py /home/jovyan/.jupyter/jupyter_notebook_config.py
