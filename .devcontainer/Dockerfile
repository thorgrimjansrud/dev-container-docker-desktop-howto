# Ubuntu bionic 
FROM mcr.microsoft.com/vscode/devcontainers/base:bionic as base

# Test multistage build
FROM scratch as final
COPY --from=base / /
CMD [ "/bin/sh" ]