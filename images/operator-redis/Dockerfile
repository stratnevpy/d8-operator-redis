ARG BASE_ALPINE
FROM quay.io/spotahome/redis-operator:v1.2.4@sha256:67935479224cb3f32628c190f1b02c5da6fe603b381cfd606270fbc3eead7a75 as artifact

FROM $BASE_ALPINE

COPY --from=artifact /usr/local/bin/redis-operator /bin/

RUN chown nobody:nogroup /bin/redis-operator

USER nobody

ENTRYPOINT ["/bin/redis-operator"]

