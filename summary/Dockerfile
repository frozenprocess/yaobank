FROM ubuntu:latest

# Install dependencies.
RUN apt-get update -y
RUN apt-get install -y python-dev build-essential curl

RUN curl -LO https://bootstrap.pypa.io/pip/2.7/get-pip.py
RUN python get-pip.py
# Copy the code into the container.
COPY ./ /app
WORKDIR /app

# Install python dependencies.
RUN pip install -r requirements.txt 

# Set the entrypoint to execute the code.
ENTRYPOINT ["python"]
CMD ["summary.py"]