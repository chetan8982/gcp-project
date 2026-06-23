FROM nginx:alpine

COPY index.html /usr/share/nginx/html/index.html

RUN cat > /etc/nginx/conf.d/default.conf <<EOF
server {
    listen 8080;
    server_name localhost;

    location / {
        root /usr/share/nginx/html;
        index index.html;
    }
}
EOF

EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]
