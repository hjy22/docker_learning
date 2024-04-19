FROM python:3.8-slim

WORKDIR /usr/service/grade-submission-application

COPY . .

RUN pip install -r grade-submission/requirements.txt

EXPOSE 5000

CMD ["python", "grade-submission/app.py"]

##往自己的docker hub上传
## docker build -t hjyyyyy22/grade-submission:flask-0.0.1 .
## docker push hjyyyyy22/grade-submission:flask-0.0.1

##拉下docker hub的image
##在仓库的tag标签下
## docker pull hjyyyyy22/grade-submission:flask-0.0.1
## docker inspect {imageID} 查看端口号
## docker run -p 8000:5000 hjyyyyy22/grade-submission:flask-0.0.1 （执行web）