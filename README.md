# postgREST
https://postgrest.org


<code>
docker run -it -d -p 3009:3000 \
  -e PGRST_DB_URI="postgres://uid:pwd@server:5555/db" \
  -e PGRST_DB_SCHEMA="public" \
  -e PGRST_DB_ANON_ROLE="role_name" \
  -e PGRST_LOG_LEVEL="info" \
  postgrest/postgrest
</code>
