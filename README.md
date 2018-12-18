# ansible_flask_demo
## Build & Run
```bash
git clone https://github.com/memo600/ansible_flask_demo.git \
&& cd ansible_flask_demo \
&& git clone https://github.com/ansible/ansible-container.git \
&& yum install python -y \
&& yum install python-pip -y \
&& pip install pipenv \
&& mkdir -p ansible-container-demo \
&& pipenv install --ignore-pipfile \
&& pipenv install ansible-container[docker] --ignore-pipfile \
&& cp -r /root/ansible_flask_demo/ansible-container/* /root/.local/share/virtualenvs/ansible_flask_demo-b9MNhOos/lib/python2.7/site-packages/container/docker/files/ \
&& pipenv shell 

$ ansible-container init  
$ ansible-container build # it may take some time on building process
$ ansible-container run

$ curl localhost:8080
```
# output
> Hello World! I have been seen 1 times.
