FROM openjdk:17-jdk-alpine
RUN addgroup -S sara && adduser -S sara -G sara && mkdir -p /opt/wezva
WORKDIR /opt/wezva
COPY . .
RUN chown -R sara:sara /opt/wezva && \
chmod +x bootstrap.sh && \
mv target/wezvatech.jar app.jar
USER sara
EXPOSE 8080
ENTRYPOINT [ "/bin/sh", "bootstrap.sh" ]