FROM ubuntu:xenial

# Set this environment variable to avoid warnings 'debconf: unable to initialize frontend: dialog'
ENV DEBIAN_FRONTEND noninteractive

    
# Install all dependencies as needed by textract. 
# Install zlibg1-dev as it is needed on docker instances.
# See http://textract.readthedocs.org/en/latest/installation.html. check note as well
RUN apt-get update && apt-get install -y \
    software-properties-common \
    python-software-properties python-pip \
    python-dev libxml2-dev libxslt1-dev \
    antiword unrtf poppler-utils pstotext tesseract-ocr \
    flac ffmpeg lame libmad0 libsox-fmt-mp3 sox libjpeg-dev swig libpulse-dev


# Install textract using pip
RUN pip install textract

ENTRYPOINT ["textract"]
