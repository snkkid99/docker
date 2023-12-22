# docker build -t snkkid/nginx .
# docker container run --name nginx -it -d -p 8080:80 --rm snkkid/nginx
# docker stop nginx
FROM nginx
COPY /Assets/ /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
