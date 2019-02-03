---

title: "Introduction: A View of Cloud Computing"

date: 2019-02-02T12:00:33+09:00

tags: ["CS349D", "Cloud Computing"]

topics: ["Cloud Computing Technology"]

---



# Introduction: A View of Cloud Computing

본 포스팅은 Stanford의 CS/EE 교수인 Christos Kozyrakis가 2018년 가을에 진행한 강의 CS349D: Cloud Computing Technology 강의노트 자료를 공부하고 요약한 내용이다. 강의 노트 원본 링크는 본문 최하단에 링크로 걸어두었다. 



### Cloud Computing의 정의

클라우드 컴퓨팅의 정의를 '대용량의 데이터 센터를 통한 컴퓨팅'으로 오해하는 경우가 많다. 하지만, 이는 엄밀한 클라우드 컴퓨팅의 정의가 아니며, '**computing as a utility**', 즉 필요할 때마다 제 3자 혹은 내부 조직으로부터 빌려 쓰는 컴퓨팅 방식이라는 의미가 클라우드 컴퓨팅의 정의이다. 



### 유형별 Cloud Service

클라우드 서비스는 서비스가 제공되는 영역에 따라 크게 3가지로 나뉜다. IaaS(Infrastructure as a Service), PaaS(Platform as a Service), SaaS(Software as a Service)가 대표 유형이다. 각 유형별로 간단히 설명하면, 

**1) IaaS: 필요한 만큼, 원하는 컴퓨팅 인프라를 쓰자**

데이터 센터를 구축하는 대신 클라우드를 활용하여 컴퓨팅 인프라를 사용하는 것을 IaaS라 한다. 고객들에게 서버 혹은 스토리지를 직접 제공하는 서비스이며, 대표적인 회사는 AWS, MS, Google, IBM등이 있다. 

IaaS는 스토리지 및 서버와 같은 인프라를 제공하고, 고객들은 인터넷을 통해 연결된 인프라에 운영체제 및 애플리케이션을 설치하고 서비스를 운영할 수 있다. 대표적인 사례로 넷플릭스를 예시로 들 수 있다. 넷플릭스는 자체 데이터센터를 구축하는 대신 AWS의 IaaS 서비스를 이용하는 방식을 택했다. 세계 주요 국가에 AWS의 데이터 센터가 있기에 각 국가별로 데이터 센터를 짓는 추가비용을 들이지 않아도 되는 이점을 누리고 있다. 국내에서는 KT, LG U+ 등이 IaaS 서비스를 운영하고 있다.

**2) PaaS: 기호에 맞춰 SW 개발 돕는, 개발자를 위한 서비스**

PaaS는 소프트웨어 개발에 필요한 플랫폼을 제공하는 서비스이다. 앞서 언급한 IaaS 보다는 조금 더 높은 레벨의 서비스이다. 이러한 서비스는 개발자들이 기반 인프라스트럭처에 대해 신경 쓰지 않고 앱을 개발하고 테스트할 수 있게 해준다. 앱을 배포하는 과정에서 서버, 스토리지, 그리고 백업 프로비저닝에 대해 걱정하는 것은 개발자 입장에서 굉장히 수고스러운 일이다. 이러한 일들을 자동으로 처리해주는 서비스가 PaaS의 역할이다. 

대표적인 PaaS 서비스 기업으로는 세일즈포스닷컴, 구글 앱엔진 등이 있다. 대표 사례로는 구글 앱엔진을 활용하는 해외의 Snapchat과 국내의 레진코믹스 기업을 예로 들 수 있다.

**3) SaaS: 필요한 소프트웨어, 설치 없이 웹에서 뚝딱**

SaaS는 클라우드 환경에서 운영되는 애플리케이션 서비스를 말한다. 즉, 모든 서비스가 클라우드에서 이뤄진다는 뜻이다. 소프트웨어를 PC에 설치하지 않아도 웹어서 소프트웨어를 빌려 쓸 수 있다. 대표적인 사례로 웹메일 서비스를 들 수 있다. email을 주고 받는 과정에서 따로 소프트웨어를 PC에 설치하지 않는다. 웹사이트를 통해 로그인하면 끝이다. 같은 예시로, 네이버 클라우드, 드롭박스 같은 클라우드 서비스도 마찬가지이다. 

대표적인 SaaS 서비스는 구글 앱스, 세일즈포스닷컴, MS오피스 365, 드롭박스 등을 들 수 있다. 

{{% fluid_img class="pure-u-1-2" src="../img_src/cloud_level.png" alt="test" %}}

위의 사진은 각 3가지 유형의 클라우드 서비스가 어떻게 다른 지 도식화한 자료이다. IaaS > PaaS > SaaS 순으로 서비스가 제공되는 영역이 좁아진다. 

최근 Amazon에는 Amazon Lambda라는 function as a service 유형이 출시되었다. 말 그대로 특정 함수를 클라우드 환경에서 대신 처리해주는 서비스이다. 이는 웹앱, IoT 앱, 스트리밍 서비스, 그리고 비디오 인코딩 등에 활용된다. 

### 클라우드 경제학: 사용자 관점

- Pay-as-you-go(usage-based) pricing
  - 클라우드 서비스는 정의대로 사용한 만큼 요금을 매긴다. 단위 시간당 혹은 단위 바이트당으로 요금을 매기는 기준은 서비스 별로 다르다. 
  - 최소 혹은 최대 요금의 정해진 bar가 없다.
  - app 사용량의 변동성이 큰 고객에게 유리하다. 
- Elasticity
  - 1000대의 서버를 1시간 동안 사용하는 요금과 1대의 서버를 1000시간 동안 사용하는 요금은 같다.
  - 따라서, 더 좋은 결과를 내기 위한 최적점을 찾아야 한다.

### 클라우드 경제학: 제공자 관점

* Economies of scale
  * 서버 장치를 구매하고 운용하는 것은 규모의 경제 효과를 누를 수 있다. 단독으로 데이터 센터를 쓰는 고객보다 운용자는 단위 유닛당 비용을 낮출 수 있다.
  * Tradeoff: 빠른 성장 vs 효율성
  * Tradeoff: 유연성 vs 비용
* Speed of itereations
  * SaaS는 빠른 업데이트, 빠른 응답시간, 그리고 세분화된 모니터링 및 피드백을 의미한다.

### 데이터센터 하드웨어

데이터 센터에 들어가는 하드웨어 구성은 다음과 같다. 

{{% fluid_img class="pure-u-1-2" src="../img_src/hardware.png" alt="test" %}}

기본적으로 한 서버에 여러대의 CPU, DRAM, 그리고 Disks가 들어가고 이러한 서버들을 40~80 개 정도 묶어 이더넷 스위치와 연결한 단위를 Rack이라 표현한다. 이러한 Rack을 다시 Switch로 수십 개 정도 묶은 것을 Cluster 단위라 표현한다. 

{{% fluid_img class="pure-u-1-2" src="../img_src/hw_compute.png" alt="test" %}}

서버의 경우 위의 사진과 같이 Multi-core CPU로 구성하는 경우가 기본이지만, 최근 머신러닝 등의 활용으로 병렬처리가 중요해졌기에 GPU, 혹은 사용처에 맞게 설계된 FPGA나 Custom accelerators를 활용하기도 한다.

{{% fluid_img class="pure-u-1-2" src="../img_src/hw_storage.png" alt="test" %}}

Storage의 경우도 기본적으로는 disk 저장장치와 SSD & Non-volatile memory를 활용하는 것이 기본이었지만, 최근 새로운 방식의 archival storage도 활용한다. 

{{% fluid_img class="pure-u-1-2" src="../img_src/hw_networking.png" alt="test" %}}

네트워킹에 쓰이는 하드웨어는 기본적으로 NIC와 switch를 기본으로 활용한다. 대부분의 네트워크는 이더넷 스위치와 라우터를 트리 형태로 배치한 구조인데 모바일 기기가 급증하고, 클라우드 기반 가상화 서비스가 등장하면서 과거와 트래픽 패턴이 달라지면서 한계가 생기기 시작했다. 이 때문에 Software defined networking(SDN)이 발전했다. 쉽게 말해 개별 네트워크 장비에서 제어 기능을 관리하는 것이 아니라 사용자가 소프트웨어로 네트워크를 제어하는 기술이다. 네트워크 제어 기능이 물리적 네트워크와 분리되어 있어 제어기능이 SDN 컨트롤러에 집중되어 있는 것이다. 

### 데이터 센터 성능 지표

데이터 센터의 성능을 나타내는 지표는 크게 Latency(지연시간), 그리고 throughput(처리량) 두 가지로 나뉜다. 두 지표를 쉽게 설명하기 위해 예시를 들어보면 다음과 같다. 

두 컴퓨터에서 같은 프로그램을 실행시킬 경우 작업이 먼저 끝나는 쪽이 빠른 컴퓨터라고 말할 수 있다. 두 컴퓨터에 하나의 프로그램이 아닌 여러 가지 프로그램을 동시에 실행 시킬 경우는 일정 시간 동안 더 많은 작업을 한 컴퓨터가 더 빠른 컴퓨터라고 말할 수 있을 것이다. 전자의 경우 Latency가 적은 컴퓨터, 후자의 경우 빠른 컴퓨터가 Throughput이 많은 컴퓨터라고
할 수 있다. 





출처(Source): [CS349D: Cloud Computing Technology](http://web.stanford.edu/class/cs349d/#projects)

