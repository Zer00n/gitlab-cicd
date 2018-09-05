# gitlab-cicd
基于gitlab and gitlab-runner，shell方式，利用maven编译打包后，落地到主机，然后用docker run运行容器。


sudo gitlab-ci-multi-runner register -n \
  --url https://gitlab.com/ \
  --registration-token REGISTRATION_TOKEN \
  --executor shell \
  --description "My Runner"
  
  gitlab-runner 基于shell
  sudo usermod -aG docker gitlab-runner
  sudo -u gitlab-runner -H docker info
  加入docker用户组，对docker有可执行权限。
