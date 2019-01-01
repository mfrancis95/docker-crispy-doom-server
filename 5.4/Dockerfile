FROM mfrancis95/chocolate-doom-build

RUN git clone -b crispy-doom-5.4 --depth 1 https://github.com/fabiangreffrath/crispy-doom && \
    cd crispy-doom && ./autogen.sh && make

FROM mfrancis95/chocolate-doom-base

COPY --from=0 /crispy-doom/src/crispy-doom /usr/local/bin/chocolate-doom