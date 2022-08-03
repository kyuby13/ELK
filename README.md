# ELK
Elasticsearch dan Kibana
--

# Jalankan docker

$ docker-compose up -d
--

# Jika elasticsearch Selalu Down cek log

docker-compose logs -f elasticsearch

nanti ada error :

elasticsearch    | ERROR: [1] bootstrap checks failed

elasticsearch    | [1]: max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]

--

# setting nysctl

sysctl -w vm.max_map_count=262144

atau 

echo "vm.max_map_count=262144" >> /etc/sysctl.conf

# Jalankan docker nya lagi
--
# Akses Kibana

http://ipaddr:5601
