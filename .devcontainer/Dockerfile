FROM apache/spark:python3

ARG CDF_PACKAGE="com.cognite.spark.datasource:cdf-spark-datasource-fatjar_2.12:3.20.1145"

USER root

# Install git
RUN apt update -y && apt install -y git

# Download CDF dependency and copy ivy cache to spark jars
RUN echo "sys.exit()" > exit.sc && \
    /opt/spark/bin/spark-shell --packages "${CDF_PACKAGE}" -I exit.sc && \
    rm exit.sc && \
    cp /root/.ivy2/jars/* /opt/spark/jars/

# Install python dependencies
RUN pip install cognite-sdk pyspark jupyter autopep8

# Create spark home and workspaces
RUN mkdir -p /home/spark /workspaces && chown spark /home/spark /workspaces

USER spark