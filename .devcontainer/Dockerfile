FROM mcr.microsoft.com/vscode/devcontainers/base:bionic as base

FROM scratch as final
COPY --from=base / /
CMD [ "/bin/sh" ]