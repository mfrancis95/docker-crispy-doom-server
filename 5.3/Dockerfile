FROM mfrancis95/chocolate-doom-build

RUN git clone -b crispy-doom-5.3 https://github.com/fabiangreffrath/crispy-doom

WORKDIR crispy-doom

RUN ./autogen.sh && make install

FROM mfrancis95/chocolate-doom-base

COPY --from=0 /usr/local/bin/crispy-doom /usr/local/bin/chocolate-doom