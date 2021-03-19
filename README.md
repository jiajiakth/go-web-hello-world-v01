# go-web-hello-world-v01
My first repository on GitHub

Summary for 10 tasks:

Task 0-Task 2 went together with Rick during the interview with system setup: base memory 8096MB, processors 4

Task 3: installed gogs; http://127.0.0.1:3000 works and created user as jiajiac in gogs

Task 4: initiated repo with a README.md and pushed the commit to master having output as: http://127.0.0.1:3000/jiajiac/go-web-hello-world

Task 5: installed kind and created a single node kubernetes cluster; installed kubectl; got cluster info,node infor and listed all pods in the cluster (the associated cmds such as kubectl config view, kebectl get pods)

by mistake, merged kubeconfig file and master file, so cehcked in master into gogs git repo instead.

Task 6: built a go web app and expose the service to 8081 port and uploaded source code as hello.go

Task 7: built a docker image and checked in the Dockerfile (using multistage) with the optimized size of container image. The size is 13.3M. using the following docker cmd and copy Dockerfile in your local folder:

1) docker build /your_local_folder -t jiajiac/go-web-hello-world 2) docker run -p 127.0.0.1:8082:8081 jiajiac/go-web-hello-world

Task 8: wrote a yaml file and tried to deployed the container image in the single node Kubernetes Uploaded the deployment.yaml for check

Task 9: Deploying the Dashboard UI: kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0/aio/deploy/recommended.yaml

Accessing the Dashboard UI: kubectl proxy

Kubectl will make Dashboard available at http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/.

try kubectl port-forward,but did not get success. so cannot change service to nodeport 31081

Regarding token generation, see https://gitlab.com/jiajiac/go-web-hello-world.git. As using private mode, maybe not seen by the link. in case, please check go-web-hello-world-master.tar that was downloaded from gitlab.

Task 10: not fully success: pushed a container image, and tried to embed gogs repo,but not sure. access by https://hub.docker.com/repository/docker/jiajiac/go-web-hello-world. The repo can be downloaded also from https://github.com/jiajiakth/go-web-hello-world-v01.
