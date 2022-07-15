# docker-cheat-sheet

# Run the container with your user

```bash
docker run \
-it \
--user $(id -u):$(id -g) \
-v /etc/passwd:/etc/passwd:ro \
-v /etc/group:/etc/group:ro \
-v $(pwd):/code \
-w /code/ \
ubuntu
```

Important bits for local user:

```bash
--user $(id -u):$(id -g) \
-v /etc/passwd:/etc/passwd:ro \
-v /etc/group:/etc/group:ro \
