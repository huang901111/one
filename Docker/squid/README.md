Squid
===

## Example:

    docker run -d --restart always -p 8081:3128 -p 8082:3129 -e SQD_USER=jiobxn -e SQD_PASS=123456 --hostname squid --name squid squid

## Run Defult Parameter
**协定：** []是默参数，<>是自定义参数

			docker run -d --restart always --privileged \\
			-p 8080:3128 \\
			-p 8443:43128 \\
			-e SQD_USER=<jiobxn> \\    用户验证访问
			-e SQD_PASS=<123456> \\    默认随机密码
			-e MAX_AUTH=[5] \\         最大验证用户数
			-e PROXY_SERVER=<"10.0.0.2,10.0.0.3"|"www.redhat.xyz|10.0.0.4;redhat.xyz|10.0.0.5"> \\  反向代理，以";"分割为一组
			-e PROXY_HTTPS=<Y> \\      后端是否启用了HTTPS
			--hostname squid \\
			--name squid squid
