FROM homeassistant/amd64-base-python:3.9-alpine3.16

# Copy files from root folder
COPY run.sh /run.sh
COPY rtl_433_mqtt_hass.py /rtl_433_mqtt_hass.py

RUN  pip install \
    --no-cache-dir \
    --prefer-binary \
    paho-mqtt

RUN chmod a+x /rtl_433_mqtt_hass.py
RUN chmod a+x /run.sh

ENTRYPOINT [ "/run.sh" ]
