## 1. Which base image do you want to use?
FROM python:3.8-slim

## 2. Set the working directory
WORKDIR "/src/app/"

## 3. Copy the project files into the working directory.
## 第一个dot表示和dockerfile同路径的所有文件，第二个dot表示workdir的路径
COPY . .

## 4. Install the dependencies
##运行在镜像本身内部去安装依赖
RUN pip install -r flask-demo/requirements.txt

## 5. Document and inform the developer that the application will use PORT 5000 of the container.
EXPOSE 5000

## 6. Define the command to run when the container starts.
## 如何执行应用程序
CMD ["python","flask-demo/app.py"]

##teminal创建镜像: 最后一个点表示寻找路径下的Dockerfile文件
##docker build -t flask-demo:0.0.1 .

##运行docker container
##docker run -p 3000:5000 flask-demo:0.0.1
##将container内部的5000端口号映射到主机的3000端口号，通过localhost:3000访问