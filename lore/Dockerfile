FROM python:3.6-jessie

LABEL maintainer='ajgil'

RUN apt-get update && \
    apt-get install -y \
    libbz2-dev \
    git

RUN pip3 install lore

RUN git clone https://github.com/montanalow/my_app.git

WORKDIR /my_app

RUN lore install

EXPOSE 5000

CMD [ "lore server &" ]

# ENTRYPOINT [ "curl", "http://localhost:5000/product_popularity.Keras/predict.json?product_name=Banana&department=produce" ] 
