# Nginx for Local Devleopment

## Objective

1. Route the traffic of `http://cssbtest.mypension.ca:8080/RestWeb/*` to remove server (`tomee`)
2. Serve the React app (`http://localhost:5173/*`) via `http://cssbtest.mypension.ca:8080/*`
3. Modify the host file to serve `cssbtest.mypension.ca` locally.

## Instructions

### 1. Modify your Host file

> You need Administrator Right to edit the host file.

For Windows: edit `C:\Windows\System32\drivers\etc\hosts`. Append the following record:

```
127.0.0.1   cssbtest.mypension.ca
```

After that, check the host mapping by `ping cssbtest.mypension.ca`.

### 2. Nginx Setup

For Windows, launch git bash and go to the same directory with this README file.

**To start:**

```sh
sh start.sh
```

Open http://localhost. Now you should see a "Welcome to nginx!" message.

**To reload:**

```sh
sh reload.sh
```

> You need to reload Nginx in order to make the changes in .conf files effective.

**To stop:** 

```sh
sh stop.sh
```

http://localhost will become unreachable and you should not see any nginx.exe in Task Manager.

