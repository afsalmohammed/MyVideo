FROM nginx:alpine
COPY nginx/nginx.conf /etc/nginx/nginx.conf
COPY --from=frontend-build /usr/share/nginx/html /usr/share/nginx/html
