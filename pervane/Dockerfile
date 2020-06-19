FROM python:slim-buster
RUN pip install pervane
RUN adduser --disabled-password --disabled-login --gecos "" pervane
RUN mkdir /home/pervane/.pervane
ADD examplesite /home/pervane/data
RUN chown -R pervane:pervane /home/pervane/data /home/pervane/.pervane
VOLUME /home/pervane/data /home/pervane/.pervane
EXPOSE 5000/tcp
USER pervane
CMD pervane --dir=/home/pervane/data/