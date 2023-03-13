FROM percona/percona-server-mongodb:3.6

ENV MONGO_INITDB_DATABASE=xhprof

RUN ["mkdir", "/docker-entrypoint-initdb.d"]
ADD xhgui.js /docker-entrypoint-initdb.d/xhgui.js
