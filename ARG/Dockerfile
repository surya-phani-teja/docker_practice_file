ARG VERSION
FROM almalinux:${VERSION:-9}
ARG COURSE="DOcker" \
    TRAINER="surya"
ENV COURSE = $"{COURSE}"
RUN echo "Trainer: ${TRAINER}, course:${COURSE}, Version: ${VERSION}"
CMD ["sleep", "1000"]
