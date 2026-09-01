FROM mcr.microsoft.com/devcontainers/base:noble

# CRIU already maintains its own dependency install scripts in the
# repo. Reuse them instead of duplicating the package list here, so
# this stays in sync with upstream automatically.
COPY contrib/apt-install /tmp/contrib/apt-install
COPY contrib/dependencies/apt-packages.sh /tmp/contrib/dependencies/apt-packages.sh
RUN /tmp/contrib/dependencies/apt-packages.sh && rm -rf /tmp/contrib /var/lib/apt/lists/*