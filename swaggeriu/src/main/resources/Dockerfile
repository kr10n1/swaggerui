FROM swaggerapi/swagger-ui:latest

COPY UI-Api.yml /usr/share/nginx/html/openapi.yaml
COPY openapi-dev.properties /usr/share/nginx/html/openapi.properties
COPY swagger-openam-stage.yml /usr/share/nginx/html/swagger-config.yaml

#ENV CONFIG_URL="swagger-config.yml"
#ENV SWAGGER_JSON_URL="openapi.yml"
#ENV SWAGGER_JSON="openapi.yml"
ENV URLS="[{url: 'openapi.yaml', name: 'Adapter'}]"
ENV PORT="8080"
ENV OAUTH2_REDIRECT_URL="https://ecadapter.dev..com/adapter/swagger/views/swagger-ui/oauth2-redirect.html"
ENV OAUTH_CLIENT_ID="urn:adapter"
ENV OAUTH_SCOPES="openid profile PPI cloudEmail preferredMail"
ENV OAUTH_USE_PKCE="true"
EXPOSE 8080