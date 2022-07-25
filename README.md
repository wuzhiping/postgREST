# postgREST
https://postgrest.org


<pre>
docker run -it -d -p 3009:3000 \
  -e PGRST_DB_URI="postgres://uid:pwd@server:5555/db" \
  -e PGRST_DB_SCHEMA="public" \
  -e PGRST_DB_ANON_ROLE="role_name" \
  -e PGRST_LOG_LEVEL="info" \
  postgrest/postgrest
</pre>

<pre>
  postgrest:
    image: postgrest/postgrest
    restart: always
    #ports:
    #  - "3000:3000"
    environment:
      PGRST_DB_URI: postgres://axelor:axelor@postgresdb:5432/axelor
      PGRST_DB_SCHEMA: public
      PGRST_DB_ANON_ROLE: axelor
      PGRST_OPENAPI_SERVER_PROXY_URI: http://www.xyz.com:3000
    depends_on:
      - postgresdb
</pre>
