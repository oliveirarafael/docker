# SonarQube

## Erros

ERROR: [1] bootstrap checks failed sonar | [1]: max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]

# Solução

sysctl -w vm.max_map_count=262144
sysctl -w fs.file-max=65536
ulimit -n 65536
ulimit -u 4096