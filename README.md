## clojurians-matrix

These repo is exploring the potential for a discovery site,
application and Matrix directory server for Clojurians Slack
community.

#### Goals

- provide infrastructure to maintain a list of rooms that are vetted by a set of administrators
- provide a web ui to browse & "discover" these rooms rooms
- provide a Matrix [directory server endpoint](https://matrix.org/docs/api/client-server/#!/Room_discovery/get_matrix_client_r0_publicRooms) that can be used by clients to provide different sets of rooms to users

#### How to run

```
boot fetch-rooms dev
```

#### Deploying

For deployment you currently need a file `clojurians-martinklepsch-com.confetti.edn` that contains AWS credentials and the name of an S3 bucket to push to. (See `deploy` for details.)

```
boot production fetch-rooms deploy
```

**Note:** a deployment of the site can be found at https://d3981087m4idf6.cloudfront.net