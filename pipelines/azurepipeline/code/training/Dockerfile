FROM tensorflow/tensorflow:2.0.0a0-py3

# pip install
COPY requirements.txt /scripts/requirements.txt
RUN pip install -r /scripts/requirements.txt

COPY train.py /scripts/train.py

# will be overwritten by kf pipeline
ENTRYPOINT [ "python", \
            "/scripts/train.py", \
            "-d", "data/train", \
            "-e", "10", \
            "-b", "32", \
            "-l", "0.0001", \
            "-o", "model", \
            "-f", "train.txt" ]
