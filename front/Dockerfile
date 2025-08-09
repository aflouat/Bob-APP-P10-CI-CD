# Build stage
FROM node:16-slim AS build

WORKDIR /usr/local/app

# Copy package.json and package-lock.json for caching
COPY package.json package-lock.json ./
RUN npm ci

# Copy the rest of the application
COPY ./ ./
RUN npm run build -- --configuration production

# Production stage
FROM nginx:1.25

# Copy custom Nginx configuration
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copy build output from build stage
COPY --from=build /usr/local/app/dist/bobapp /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
