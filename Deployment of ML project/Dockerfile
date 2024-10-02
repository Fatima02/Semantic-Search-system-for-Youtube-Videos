# start from python base image
FROM python:3.10

# change working directory
WORKDIR /code

# add requirements file to image
COPY ./requirements.txt /code/requirements.txt

# install python libraries
RUN pip install --no-cache-dir --upgrade -r requirements.txt --log install.log

# add python code
COPY ./app/ /code/app/

# specify default commands
#CMD ["fastapi", "run", "app/main.py", "--port", "80"]

# Command to run your application
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]