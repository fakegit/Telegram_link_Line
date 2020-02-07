FROM python:3.6
MAINTAINER we684123
# for image_conversion

RUN python -m pip install --upgrade pip \
    && pip install filetype==1.0.5 \
    flask==1.1.1 \
    flask-restful==0.3.8 \
    Pillow==7.0.0 \
    uwsgi==2.0.18 \
    && mkdir -p /image_conversion/conversion用

COPY ./main.py /image_conversion/main.py
COPY ./mylib /image_conversion/mylib
COPY ./uWSGI/image_conversion.ini /image_conversion/image_conversion.ini

EXPOSE 5000

CMD ["uwsgi","/image_conversion/image_conversion.ini"]
