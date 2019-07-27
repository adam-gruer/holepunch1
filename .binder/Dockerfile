FROM rocker/binder:3.6.0
LABEL maintainer='Adam Gruer'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}
RUN R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-07-27/')); devtools::install_deps()"
