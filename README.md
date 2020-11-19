## install elastic search

https://www.elastic.co/guide/en/elasticsearch/reference/current/deb.html

## elasticsearch 실행 시 jre 메모리 부족하다고 뜰때

[자바 메모리 설정 방법]

https://steady-snail.tistory.com/120

[elasticsearch 요구 메모리 수정 방법]

https://www.elastic.co/guide/en/elasticsearch/reference/current/important-settings.html#heap-size-settings

## elasticsearch 실행 오류

[discovery settings are unsuitable for production]

https://stackoverflow.com/questions/59350069/elasticsearch-start-up-error-the-default-discovery-settings-are-unsuitable-for

## 실행한 명령어
```
sudo apt update
sudo apt install openjdk-8-jdk -y

curl -s https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -

sudo apt-get install apt-transport-https
echo "deb https://artifacts.elastic.co/packages/6.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-6.x.list

sudo apt-get update
sudo apt-get install elasticsearch -y

sudo usermod -a -G elasticsearch ubuntu

cd /etc/elasticsearch
vim elasticsearch.yml
vim jvm.options
sudo systemctl restart elasticsearch

sudo apt-get install kibana
sudo usermod -a -G kibana ubuntu

cd /etc/kibana

sudo apt-get install logstash
```

