# This file is generated by Nx.
#
# Build the docker image with `npx nx docker-build techradar-ui`.
# Tip: Modify "docker-build" options in project.json to change docker build args.
#
# Run the container with `docker run -p 3000:3000 -t techradar-ui`.
FROM docker.io/node:lts-alpine

ENV HOST=0.0.0.0
ENV PORT=3000

WORKDIR /app

RUN addgroup --system techradar-ui && \
          adduser --system -G techradar-ui techradar-ui

COPY  apps/techradar-ui techradar-ui
COPY  node_modules techradar-ui/node_modules
RUN chown -R techradar-ui:techradar-ui .

USER techradar-ui

CMD ["node", "techradar-ui/.output/server/index.mjs"]
