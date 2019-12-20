#### run with container

```bash
git clone https://github.com/jobscale/cdn.git
cd cdn
main() {
  docker build . -t local/cdn:0.0.1
  docker run --rm --name cdn -p 8443:443 -d local/cdn:0.0.1
  sleep 0.8
  curl -k https://127.0.0.1:8443
  docker stop cdn
} && main
```
