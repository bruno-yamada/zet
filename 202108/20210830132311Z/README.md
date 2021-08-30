# Sample nginx configuration with JSON log output

When sending logs to some aggregators it might facilitate to have the logs printed as JSON instead of the traditional format, as dealing with JSON would make query easier on those platforms, still, when querying logs in the application through more direct ways, you might have to leverage jq


nginx.conf:
```
user  nginx;
worker_processes  auto;

error_log  /var/log/nginx/error.log warn;
pid        /var/run/nginx.pid;

events {
    worker_connections  1024;
}

http {
    include       /etc/nginx/mime.types;
    default_type  application/octet-stream;

    log_format main_json escape=json '{'
      '"msec": "$msec", ' # request unixtime in seconds with a milliseconds resolution
      '"connection": "$connection", ' # connection serial number
      '"connection_requests": "$connection_requests", ' # number of requests made in connection
      '"request_id": "$request_id", ' # the unique request id
      '"request_length": "$request_length", ' # request length (including headers and body)
      '"remote_addr": "$remote_addr", ' # client IP
      '"remote_user": "$remote_user", ' # client HTTP username
      '"remote_port": "$remote_port", ' # client port
      '"time_iso8601": "$time_iso8601", ' # local time in the ISO 8601 standard format
      '"request": "$request", ' # full path no arguments if the request
      '"request_uri": "$request_uri", ' # full path and arguments if the request
      '"status": "$status", ' # response status code
      '"bytes_sent": "$bytes_sent", ' # the number of bytes sent to a client
      '"http_referer": "$http_referer", ' # HTTP referer
      '"http_user_agent": "$http_user_agent", ' # user agent
      '"http_x_forwarded_for": "$http_x_forwarded_for", ' # http_x_forwarded_for
      '"http_host": "$http_host", ' # the request Host: header
      '"server_name": "$server_name", ' # the name of the vhost serving the request
      '"request_time": "$request_time", ' # request processing time in seconds with msec resolution
      '"upstream": "$upstream_addr", ' # upstream backend server for proxied requests
      '"upstream_connect_time": "$upstream_connect_time", ' # upstream handshake time incl. TLS
      '"upstream_header_time": "$upstream_header_time", ' # time spent receiving upstream headers
      '"upstream_response_time": "$upstream_response_time", ' # time spend receiving upstream body
      '"upstream_response_length": "$upstream_response_length", ' # upstream response length
      '"upstream_cache_status": "$upstream_cache_status", ' # cache HIT/MISS where applicable
      '"ssl_protocol": "$ssl_protocol", ' # TLS protocol
      '"ssl_cipher": "$ssl_cipher", ' # TLS cipher
      '"scheme": "$scheme", ' # http or https
      '"request_method": "$request_method", ' # request method
      '"server_protocol": "$server_protocol" ' # request protocol, like HTTP/1.1 or HTTP/2.0
    '}';

    access_log  /var/log/nginx/access.log main_json;

    sendfile        on;

    keepalive_timeout  65;

    server {
        listen       80;

        # Auth
        location / {
            proxy_pass http://my-app;
        }

        # Health-check
        location /ping {
            add_header Content-Type text/plain;
            return 200 'pong';
        }
    }
}
```

> tags: nginx; json;

> uid: 20210830132311Z

> links: 

