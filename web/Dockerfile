FROM nginx:latest
RUN rm /usr/share/nginx/html/index.html
ADD static /usr/share/nginx/html/
COPY roboshop.conf /etc/nginx/conf.d/roboshop.conf
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]