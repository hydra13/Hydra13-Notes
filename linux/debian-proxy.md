Задание настроек прокси-сервера в Debian
/etc/profile.d/proxy.sh:
export http_proxy=http://192.168.0.1:3128
/etc/apt/apt.conf.d/99HttpProxy:
Acquire::http::Proxy "http://192.168.0.1:3128";
/etc/wgetrc:
http_proxy = http://192.168.0.1:3128
