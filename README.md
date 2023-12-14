## Related Repositories

<table>
  <tr>
    <td colspan=2 align=center>플랫폼</td>
    <td colspan=2 align=center><a href="https://github.com/K-PaaS/cp-deployment">컨테이너 플랫폼</a></td>
    <td colspan=2 align=center><a href="https://github.com/K-PaaS/sidecar-deployment">사이드카</a></td>
    <td colspan=2 align=center><a href="https://github.com/K-PaaS/ap-deployment">어플리케이션 플랫폼</a></td>
  </tr>
  <tr>
    <td colspan=2 align=center>포털</td>
    <td colspan=2 align=center><a href="https://github.com/K-PaaS/cp-portal-release">CP 포털</a></td>
    <td colspan=2 align=center>-</td>
    <td colspan=2 align=center><a href="https://github.com/K-PaaS/portal-deployment">AP 포털</a></td>
  </tr>
  <tr align=center>
    <td colspan=2 rowspan=9>Component<br>/ 서비스</td>
    <td colspan=2><a href="https://github.com/K-PaaS/cp-portal-common-api">Common API</a></td>
    <td colspan=2>-</td>
    <td colspan=2><a href="https://github.com/K-PaaS/ap-mongodb-shard-release">🚩 MongoDB</a></td>
  </tr>
  <tr align=center>
    <td colspan=2><a href="https://github.com/K-PaaS/cp-metrics-api">Metric API</a></td>
    <td colspan=2>  </td>
    <td colspan=2><a href="https://github.com/K-PaaS/ap-mysql-release">MySQL</a></td>
  </tr>
  <tr align=center>
    <td colspan=2><a href="https://github.com/K-PaaS/cp-portal-api">Portal API</a></td>
    <td colspan=2>  </td>
    <td colspan=2><a href="https://github.com/K-PaaS/ap-pipeline-release">Pipeline</a></td>
  </tr>
  <tr align=center>
    <td colspan=2><a href="https://github.com/K-PaaS/cp-portal-ui">Portal UI</a></td>
    <td colspan=2>  </td>
    <td colspan=2><a href="https://github.com/K-PaaS/ap-rabbitmq-release">RabbintMQ</a></td>
  </tr>
  <tr align=center>
    <td colspan=2><a href="https://github.com/K-PaaS/cp-portal-service-broker">Service Broker</a></td>
    <td colspan=2>  </td>
    <td colspan=2><a href="https://github.com/K-PaaS/ap-on-demand-redis-release">Redis</a></td>
  </tr>
  <tr align=center>
    <td colspan=2><a href="https://github.com/K-PaaS/cp-terraman">Terraman API</a></td>
    <td colspan=2>  </td>
    <td colspan=2><a href="https://github.com/K-PaaS/ap-source-control-release">SoureceControl</a></td>
  </tr>
</table>
<i>🚩 You are here.</i>

## Notice
#### 릴리즈의 경로가 https://nextcloud.paas-ta.org/ 에서 https://nextcloud.k-paas.org/ 로 변경되었습니다  



  

  


## ap-mongodb-shard-release

### Application Platform MongoDB Shard Release Configuration
  - mongodb_broker : 1 machine  
  - mongodb_shard : 1 machine  
  - mongodb_config : N machine(s)  
  - mongodb_master : N machine(s)  
  - mongodb_slave : N machine(s)  

### Create Application Platform MongoDB Shard Release
  - Download the latest Application Platform MongoDB Shard Release
    ```  
    $ git clone https://github.com/K-PaaS/ap-mongodb-shard-release.git
    $ cd ap-mongodb-shard-release
    ```  
  - Download & Copy "source files" into the src directory
    ```
    ## download source files
    $ wget -O src.zip https://nextcloud.k-paas.org/index.php/s/m3oJzNbD8axKFKR/download
    
    ## unzip download source files
    $ unzip src.zip 
    
    ## final src directory
    src  
        ├── cli
        │   └── cf-linux-amd64-6.10.0.tgz
        ├── java7
        │   └── jre-7u45-linux-x64.gz
        ├── mongodb
        │   ├── libssl1.1_1.1.1f-1ubuntu2.19_amd64.deb
        │   └── mongodb-linux-x86_64-ubuntu1804-4.2.17.tgz
        └── ap-mongodb-broker
            └── ap-mongodb-broker.jar
    ```
  - Create Application Platform MongoDB Shard Release
    ```  
    ## <VERSION> :: release version (e.g. 2.1.2)
    ## <RELEASE_TARBALL_PATH> :: release file path (e.g. /home/ubuntu/workspace/ap-mongodb-shard-release-<VERSION>.tgz)
    $ bosh -e <bosh_name> create-release --name=ap-mongodb-shard --version=<VERSION> --tarball=<RELEASE_TARBALL_PATH> --force

    ```   


## Contributors ✨

<a href="https://github.com/K-PaaS/ap-mongodb-shard-release/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=K-PaaS/ap-mongodb-shard-release" />
</a>
