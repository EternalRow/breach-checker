https://github.com/EternalRow/breach-checker/actions/runs/45919852227/job/140247733335
ERROR: failed to build: failed to solve: process "/bin/sh -c htmlhint index.html" did not complete successfully: exit code: 1

https://github.com/EternalRow/breach-checker/actions/runs/45920001587



https://github.com/EternalRow/breach-checker/actions/runs/45925746026
Run curl --fail -sS http://localhost:8080/api/health
curl: (22) The requested URL returned error: 502
Error: Process completed with exit code 22.

https://github.com/EternalRow/breach-checker/actions/runs/45927205766

Po nieudanym uruchomieniu tag latest wskazywał na wersję sprzed commita, jest to istotne, żeby osoba pobierająca najnowszy obraz nie pobrała programu zawierającego błędy

docker pull ghcr.io/eternalrow/breach-checker-backend:latest
latest: Pulling from eternalrow/breach-checker-backend
0ba51f9c0aed: Pull complete 
e3e428093f5e: Pull complete 
cefca11dff4e: Pull complete 
5d30ed3b6f7e: Pull complete 
286d8c291daa: Pull complete 
ae199f1d3d03: Pull complete 
b05b4664f667: Pull complete 
83a14706aa6d: Pull complete 
30cf67d7101c: Pull complete 
Digest: sha256:774211b0d5ce5628edbc88fee7a5351596b3b8ea8bf74e43c349afb023123b30
Status: Downloaded newer image for ghcr.io/eternalrow/breach-checker-backend:latest
ghcr.io/eternalrow/breach-checker-backend:latest



docker pull ghcr.io/eternalrow/breach-checker-backend:2c5f5c21316a4795bf48b1aa0b4ac5caddcff1ec
2c5f5c21316a4795bf48b1aa0b4ac5caddcff1ec: Pulling from eternalrow/breach-checker-backend
Digest: sha256:774211b0d5ce5628edbc88fee7a5351596b3b8ea8bf74e43c349afb023123b30
Status: Downloaded newer image for ghcr.io/eternalrow/breach-checker-backend:2c5f5c21316a4795bf48b1aa0b4ac5caddcff1ec
ghcr.io/eternalrow/breach-checker-backend:2c5f5c21316a4795bf48b1aa0b4ac5caddcff1ec



docker images --digests ghcr.io/eternalrow/breach-checker-backend
REPOSITORY                                  TAG                                        DIGEST                                                                    IMAGE ID       CREATED         SIZE
ghcr.io/eternalrow/breach-checker-backend   2c5f5c21316a4795bf48b1aa0b4ac5caddcff1ec   sha256:774211b0d5ce5628edbc88fee7a5351596b3b8ea8bf74e43c349afb023123b30   774211b0d5ce   8 minutes ago   212MB
ghcr.io/eternalrow/breach-checker-backend   latest                                     sha256:774211b0d5ce5628edbc88fee7a5351596b3b8ea8bf74e43c349afb023123b30   774211b0d5ce   8 minutes ago   212MB



docker push ghcr.io/eternalrow/breach-checker-backend:latest
The push refers to repository [ghcr.io/eternalrow/breach-checker-backend]
83a14706aa6d: Layer already exists 
286d8c291daa: Layer already exists 
30cf67d7101c: Layer already exists 
e3e428093f5e: Layer already exists 
ae199f1d3d03: Layer already exists 
cefca11dff4e: Layer already exists 
b05b4664f667: Layer already exists 
0ba51f9c0aed: Layer already exists 
5d30ed3b6f7e: Layer already exists 
latest: digest: sha256:774211b0d5ce5628edbc88fee7a5351596b3b8ea8bf74e43c349afb023123b30 size: 2199

Token służył do nadpisywania stanu pakietów, w zależności od nadawanych uprawnień, istneje możliwość odczytu. Tutaj zadziałały zarówno push, jak i pull, z powodu uprawnienia write:packages