## Docker build for NGINX Plus
`docker build -f Dockerfile --no-cache --secret id=nginx-key,src=nginx-repo.key --secret id=nginx-crt,src=nginx-repo.crt -t nplus-unprivileged .`

## Docker build for NGINX Plus with NGINX Agent
`docker build -f Dockerfile --no-cache --secret id=nginx-key,src=nginx-repo.key --secret id=nginx-crt,src=nginx-repo.crt --build-arg NMS_URL=https://<nms_ip_address> --build-arg NMS_GROUP=<instance_group_name> -t nplus-unprivileged-agent .`
