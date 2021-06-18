FROM rocker/r-base:4.1.0

RUN /rocker_scripts/install_tidyverse.sh

RUN /rocker_scripts/install_geospatial.sh

CMD ["/init"]

COPY scripts/install_img_video.sh /rocker_scripts/install_img_video.sh

RUN /rocker_scripts/install_img_video.sh