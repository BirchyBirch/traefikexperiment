# Traefik on windows
1. get NSSM https://nssm.cc/release/nssm-2.24.zip
2. get traefik https://github.com/containous/traefik/releases
3. create your traefik run directory, e.g. D:\traefik
4. copy traefik.exe, traefik.yml and dynamic-conf.yml to traefik run directory
5. use NSSM to create a traefik service: 
    1. nssm install traefikccb "d:\traefik\traefik.exe"
    2. nssm set traefik appparameters "--configFile=d:\traefik\traefik.yml"
6. start traefik service
7. open: http://traefik.localhost/dashboard/#/
8. configure the url for the target item in dynamic-conf.yml