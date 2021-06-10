FROM rocker/rstudio:4.1.0

LABEL org.opencontainers.image.licenses="GPL-2.0-or-later" \
      org.opencontainers.image.source="https://github.com/rocker-org/rocker-versioned2" \
      org.opencontainers.image.vendor="Rocker Project" \
      org.opencontainers.image.authors="Carl Boettiger <cboettig@ropensci.org>"

RUN /rocker_scripts/install_tidyverse.sh

RUN /rocker_scripts/install_geospatial.sh

ENV S6_VERSION=v1.21.7.0
ENV SHINY_SERVER_VERSION=latest
ENV PANDOC_VERSION=default

RUN /rocker_scripts/install_shiny_server.sh

EXPOSE 3838

CMD ["/init"]

COPY ../../scripts/install_img_video.sh /rocker_scripts/install_img_video.sh

RUN /rocker_scripts/install_img_video.sh