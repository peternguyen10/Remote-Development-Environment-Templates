ARG VERSION="latest"
ARG INSTALL_MAVEN='false'
ARG INSTALL_GRADLE='false'

# Full list of tags can be found at https://github.com/docker-library/docs/blob/master/openjdk/README.md#supported-tags-and-respective-dockerfile-links
FROM openjdk:${VERSION}

# Specify whether container comes with build tools (optional)
# These commands should be modified if running a non-Debian version of the image
RUN if [ "${INSTALL_MAVEN}" = "true" ]; then su vscode -c "source /usr/local/sdkman/bin/sdkman-init.sh && sdk install maven \"${MAVEN_VERSION}\""; fi \
    && if [ "${INSTALL_GRADLE}" = "true" ]; then su vscode -c "source /usr/local/sdkman/bin/sdkman-init.sh && sdk install gradle \"${GRADLE_VERSION}\""; fi
