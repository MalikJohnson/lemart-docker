# Use Nginx to serve the already-built Angular app
FROM nginx:alpine

RUN rm -rf /usr/share/nginx/html/*
COPY dist/le-mart-app/browser /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]


