# Heroku Database Support

Sometimes you need to edit the Database manually, This is not something you should be playing around with unless you really know what you are doing.

## Step 1 - Checklist <a id="step-1---checklist"></a>

1. Know that you are doing, if you don’t then **don’t** touch the DB. Simple.
2. Download and Install Postgres Admin 4, Located [Here](https://www.pgadmin.org/download/) or [Here](https://www.postgresql.org/ftp/pgadmin/pgadmin4/). _This guide will be for Windows, but it shouldn’t be much different for any other OS._
3. Locate your credentials for you Heroku Database, Log in to **Heroku** &gt; Select your **App** &gt; Click **Resources** &gt; Click **Heroku Postgres** &gt; Click **Settings** &gt; Click **View Credentials** \(_Note: Heroku rotates credentials periodically and updates applications where this database is attached._\)

## Step 2 - Connect <a id="step-2---connect"></a>

For a fresh install of pgAdmin, the dashboard likely contains only one server. This is your local server, Ignore this.

1. Right click server\(s\) &gt; create &gt; server …
2. Fill out the following:
   * **Name:** This is solely for you. Name it whatever you want, I chose ‘Heroku-Run — On’

_Under the connection tab:_

* **Hostname/Address:** This is the host credential you located in Step 3. It should look like \*\*-\*\*-\*\*…amazonaws.com
* **Port:** Keep the port at 5432, unless your credentials list otherwise
* **Maintenance databaseL** This is the database field located in Step 3 Below.
* **Username:** This is the user field in the credentials
* **Password:** The password field located in Step 3. I highly advise checking save password so that you don’t have to copypasta this every time you want to connect.
* In the **SSL Tab**, mark SSL mode as require

At this point, if we were to hit ‘save’ \(please don’t\), something very strange would happen. You’d see hundreds if not thousands of databases appear in pgAdmin. This has to do with how Heroku configures their servers. You’ll still only have access to your specific database, not those of others. In order to avoid parsing so many databases, we have to white list only those databases we care about.

1. Go to the **Advanced** tab and under db restriction copy the database name \(it’s the same value as the **Maintenance Database** field filled earlier\).
2. Click Save/Connect and you are done. Edit away.

