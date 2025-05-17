# Stage 1: Build the Angular app
FROM node:20 as build

WORKDIR /app
COPY . .
RUN npm install
RUN npm run build --prod

# Stage 2: Serve the app with Nginx
FROM nginx:alpine

RUN rm -rf /usr/share/nginx/html/*
COPY --from=build /app/dist/le-mart-app/browser /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]

