Run ssh ***@*** << 'ENDSSH'
Pseudo-terminal will not be allocated because stdin is not a terminal.
Welcome to Ubuntu 24.04.4 LTS (GNU/Linux 6.8.0-107-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Sat Apr  4 14:48:44 UTC 2026

  System load:  0.12               Processes:             154
  Usage of /:   15.5% of 47.39GB   Users logged in:       1
  Memory usage: 29%                IPv4 address for eth0: ***
  Swap usage:   0%                 IPv6 address for eth0: 2a02:4780:10:cf48::1

 * Strictly confined Kubernetes makes edge and IoT secure. Learn how MicroK8s
   just raised the bar for easy, resilient and secure K8s cluster deployment.

   https://ubuntu.com/engage/secure-kubernetes-at-the-edge

Expanded Security Maintenance for Applications is not enabled.

5 updates can be applied immediately.
To see these additional updates run: apt list --upgradable

Enable ESM Apps to receive additional future security updates.
See https://ubuntu.com/esm or run: sudo pro status


1 updates could not be installed automatically. For more details,
see /var/log/unattended-upgrades/unattended-upgrades.log

▶ Rebuilding containers...
 Image deploy-migrate Building 
 Image deploy-api Building 
 Image deploy-platform Building 
#1 [internal] load local bake definitions
#1 reading from stdin 1.53kB done
#1 DONE 0.0s

#2 [platform internal] load build definition from Dockerfile.platform
#2 transferring dockerfile: 1.76kB done
#2 DONE 0.0s

#3 [api internal] load build definition from Dockerfile.api
#3 transferring dockerfile: 2.25kB done
#3 DONE 0.0s

#4 [migrate internal] load build definition from Dockerfile.migrate
#4 transferring dockerfile: 621B 0.0s done
#4 DONE 0.1s

#5 [migrate internal] load metadata for docker.io/library/node:20-alpine
#5 DONE 0.5s

#6 [platform internal] load metadata for docker.io/library/nginx:alpine
#6 DONE 0.5s

#7 [api internal] load .dockerignore
#7 transferring context: 2B done
#7 DONE 0.0s

#8 [migrate internal] load build context
#8 DONE 0.0s

#9 [platform internal] load build context
#9 ...

#10 [api internal] load build context
#10 transferring context: 542.64kB 0.2s done
#10 DONE 0.2s

#9 [platform internal] load build context
#9 transferring context: 1.45MB 0.2s done
#9 DONE 0.2s

#11 [platform builder 12/17] COPY lib/api-client-react/ lib/api-client-react/
#11 CACHED

#12 [platform builder  3/16] WORKDIR /app
#12 CACHED

#13 [platform builder 13/17] COPY artifacts/platform/   artifacts/platform/
#13 CACHED

#14 [platform builder  5/17] COPY lib/db/package.json               lib/db/
#14 CACHED

#15 [platform builder  7/17] COPY lib/api-client-react/package.json lib/api-client-react/
#15 CACHED

#16 [platform builder 10/17] COPY lib/db/               lib/db/
#16 CACHED

#17 [platform builder  2/16] RUN npm install -g pnpm@9
#17 CACHED

#18 [platform builder  8/17] COPY artifacts/platform/package.json   artifacts/platform/
#18 CACHED

#19 [platform builder 17/17] RUN pnpm --filter @workspace/platform run build
#19 CACHED

#20 [platform builder  9/17] RUN pnpm install --frozen-lockfile                  --filter @workspace/api-client-react...                  --filter @workspace/platform...
#20 CACHED

#21 [platform builder 15/17] COPY tsconfig.base.json    ./
#21 CACHED

#22 [platform builder 14/17] COPY attached_assets/      attached_assets/
#22 CACHED

#23 [platform builder  6/17] COPY lib/api-zod/package.json          lib/api-zod/
#23 CACHED

#24 [platform builder  4/17] COPY package.json pnpm-workspace.yaml pnpm-lock.yaml ./
#24 CACHED

#25 [platform builder 11/17] COPY lib/api-zod/          lib/api-zod/
#25 CACHED

#26 [platform builder 16/17] COPY tsconfig.json         ./
#26 CACHED

#27 [platform runtime 2/3] COPY --from=builder /app/artifacts/platform/dist/public /usr/share/nginx/html
#27 CACHED

#28 [platform runtime 3/3] COPY nginx-spa.conf /etc/nginx/conf.d/default.conf
#28 ERROR: failed to calculate checksum of ref i39xbwwkdeygcnbel2q5hwgil::sgt4m74j1moiju9i5bhf3wnwl: "/nginx-spa.conf": not found

#29 [platform runtime 1/3] FROM docker.io/library/nginx:alpine@sha256:e7257f1ef28ba17cf7c248cb8ccf6f0c6e0228ab9c315c152f9c203cd34cf6d1
#29 resolve docker.io/library/nginx:alpine@sha256:e7257f1ef28ba17cf7c248cb8ccf6f0c6e0228ab9c315c152f9c203cd34cf6d1 0.2s done
#29 CANCELED

#8 [migrate internal] load build context
#8 transferring context: 265.18kB 0.0s done
#8 DONE 0.1s

#17 [api builder  2/16] RUN npm install -g pnpm@9
#17 CACHED

#30 [api builder  7/16] COPY lib/api-client-react/package.json    lib/api-client-react/
#30 CACHED

#31 [api builder  6/16] COPY lib/api-zod/package.json             lib/api-zod/
#31 CACHED

#32 [api builder  4/16] COPY package.json pnpm-workspace.yaml pnpm-lock.yaml ./
#32 CACHED

#12 [api builder  3/16] WORKDIR /app
#12 CACHED

#33 [api builder  8/16] COPY artifacts/api-server/package.json    artifacts/api-server/
#33 CANCELED

#34 [migrate builder  5/16] COPY lib/db/package.json                  lib/db/
#34 CANCELED

#35 [migrate builder  1/16] FROM docker.io/library/node:20-alpine@sha256:f598378b5240225e6beab68fa9f356db1fb8efe55173e6d4d8153113bb8f333c
#35 resolve docker.io/library/node:20-alpine@sha256:f598378b5240225e6beab68fa9f356db1fb8efe55173e6d4d8153113bb8f333c 0.2s done
------
 > [platform runtime 3/3] COPY nginx-spa.conf /etc/nginx/conf.d/default.conf:
------
WARNING: current commit information was not captured by the build: failed to read current commit information with git rev-parse --is-inside-work-tree

WARNING: current commit information was not captured by the build: failed to read current commit information with git rev-parse --is-inside-work-tree

WARNING: current commit information was not captured by the build: failed to read current commit information with git rev-parse --is-inside-work-tree

Dockerfile.platform:45

--------------------

  43 |     COPY --from=builder /app/artifacts/platform/dist/public /usr/share/nginx/html

  44 |     

  45 | >>> COPY nginx-spa.conf /etc/nginx/conf.d/default.conf

  46 |     

  47 |     EXPOSE 3000

--------------------

target platform: failed to solve: failed to compute cache key: failed to calculate checksum of ref i39xbwwkdeygcnbel2q5hwgil::sgt4m74j1moiju9i5bhf3wnwl: "/nginx-spa.conf": not found

Error: Process completed with exit code 1.