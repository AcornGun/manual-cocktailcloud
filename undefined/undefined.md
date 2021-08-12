# 클러스터 관리

## ​플랫폼 관리 - 클러스터 관리 

클러스터의 주요 구성요소는 노드, 스토리지, 애플리케이션 입니다. 구성한 클러스터가 계획에 따라 동작하도록 관리하기 위해서는 모니터링과 알림 그리고 보안 설정이 추가로 필요합니다.

클러스터 관리에 필요한 도구와 내용을 하나씩 살펴 보도록 하겠습니다. 

메뉴이동: ←클러스터

![\[&#xD654;&#xBA74;\] &#xD074;&#xB7EC;&#xC2A4;&#xD130; &#xAD00;&#xB9AC;](../.gitbook/assets/2020-10-20-10.50.12.png)

## 클러스터 관리 화면에서 제공되는 정보 및 기능

> * 클러스터 공급자\(Cloud Service Provider\) 종류, 물리적 위치\(지역\)
> * 클러스터 동작 상태 \(Running/Stop\)
> * 클러스터 자원 할당 유형 \(클러스터/서비스 맵\)
> * 클러스터 할당 노드 수
> * 클러스터 할당 자원
> * 클러스터 할당 워크스페이스 수
> * 클러스터 발생 알림 
> * \[기능\] 클러스터 등록
> * \[기능\] 클러스터 웹 접속 터미널 연결 링크
> * \[기능\] 클러스터 외부 접속 인증서 다운로드

## 클러스터 등록은 어떻게 하나요?

칵테일 클라우드는 온-프레미스 환경\(물리적 서버\) 과 클라우드 서비스에 구 가능하며, 지속적으로 추가 연동을 개발하고 있습니다.

> * On-Premise \(물리서버\)
> * Amazon Web Service
> * Google Cloud Platform
> * Microsoft Azure
> * Alibaba Cloud
> * Tencent Cloud
> * Rovius Cloud

클러스터 등록\(생성\) 은 아래 링크에서 상세히 설명하고 있습니다.

{% embed url="https://app.gitbook.com/@cocktailcloud/s/cocktail-cloud-kr/undefined-2/undefined" caption="\[링크\] 클러스터등록" %}

## 클러스터에 할당된 자원 현황은 어떻게 확인 할 수 있나요?

등록된 클러스터의 자원과 상태를 확인하기 위해서 클러스터 목록 화면으로 이동합니다. 

메뉴이동: ⓦ 플랫폼 관리 &gt; ←클러스터

클러스터 목록 화면에서 접근 가능한 클러스터의 목록이 표시됩니다. 

![\[&#xD654;&#xBA74;\] &#xC811;&#xADFC; &#xAC00;&#xB2A5;&#xD55C; &#xD074;&#xB7EC;&#xC2A4;&#xD130; &#xBAA9;&#xB85D; &#xBC0F; &#xC790;&#xC6D0; &#xD604;&#xD669;](../.gitbook/assets/2020-10-20-10.50.12.png)

클러스터 목록 화면 제공 정보

> * 클러스터 이름 \(사용자 지정\)
> * 공급자, 지역 \(클라우드 서비스 프로바이더 구분, 물리적 위치 및 리전\)
> * 상태 \(Running, Stop\)
> * 자원 할당 유형 \(플랫폼, 클러스터, 서비스 맵\)
> * 노드 수 \(클러스터 구성 노드 수\)
> * 클러스터 자원 \(CPU, Memory, Storage\) 현황
> * 워크스페이스 \(클러스터 자원\)
> * 알람 \(발생된 알람 수\)

## 클러스터 구성 자원의 상세 자원 현황은 어떻게 확인 하나요?

등록된 클러스터의 구성 자원을 변경하거나 등록 정보를 변경하기 위해서 등록 정보 화면으로 이동합니다. 

메뉴이동: ⓦ 플랫폼 관리 &gt; ←클러스터 &gt; \(클러스터 선택\) &gt; ↑개요 &gt; 등록정보 화면

### Step 1. 클러스터 구성 개요 확인하기 클러스터 등록정보 화면에서 설정 가능한 정보

> * \(클라우드서비스\) 프로바이더
> * \(클라우드서비스\) 서비스 유형
> * 서브스크립션 아이디 \(Azure AKS 선택 입력\)
> * 프로젝트 아이디 \(Google GKE 선택 입력\)
> * 클러스터 \(클러스터 이름\)
> * 리전 \(프로바이더 및 서버의 지역적/물리적 위치\)
> * 클러스터 이름 \(칵테일 클라우드에서 표현될 이름\)
> * 쿠버네티스 버전 \(클러스터에서 사용하는 쿠버네티스 버전 정보\)
> * 아이디 \(클러스터 공유 아이디, 알라메시지 리다이렉트 시 필요\)
> * 설명 \(클러스터에 대한 사용자 설명을 추가\)
> * 마스터 주소 \(Kubernetes API 주소. “ [https://host:port](https://host:port/) ” 형식을 사용한다.\)
> * 인그레스 호스트 \(인그레스 방식에 사용할 Host IP Address 서비스, Master IP or Load balancer IP\)
> * 노드 포트 호스트 주소 \(노드에 포트를 붙여 서비스 노출하는 방식에서 포트 앞에 사용할 IP서비스, Master IP or Load balancer IP\)
> * 노드 포트 범위 \(노드에 포트를 붙여 서비스 노출하는 방식에서 IP뒤에 사용할 포트의 범위, 30000~32767 권장\)
> * Cluster CA Certification \(마스터 서버 접속 후 /etc/kubernetes/pki 경로 이동 후 ca.crt파일값 입력\)
> * Client Certificate Data \(마스터 서버 접속 후 /etc/kubernetes/pki 경로 이동 후 admin.crt파일 값 입력\)
> * Client Key Data \(마스터 서버 접속 후 /etc/kubernetes/pki 경로 이동 후 admin.key파일 값 입력\)

### Step 2. 클러스터 구성 노드의 자원 모니터링 확인하기 등록된 클러스터의 노드 자원 정보를 확인하기위해서 노드 상세 화면으로 이동합니다. 

메뉴이동: ⓦ 플랫폼 관리 &gt; ←클러스터 &gt; \(클러스터 선택\) &gt; ↑노드 &gt; 노드 목록 &gt; \(노드 이름 선택\) &gt; 모니터링 화면

자원 사용 현황\(CPU, Memory, Disk, 네트워크\), 자원 요약\(용량, 가용량, 요청량\), 상태\(이벤트 발생에 따른 유형, 상태, 최근 발생 시간, 최근 경과시간, 발생 이유, 메시지\) 정보가 제공 됩니다. 노드에 대한 모니터링 정보는 통합 모니터링 메뉴에서도 추가적인 정보를 얻을 수 있습니다

{% embed url="https://app.gitbook.com/@cocktailcloud/s/cocktail-cloud-kr/undefined/undefined-4" caption="\[링크\] 통합 모니터링" %}

### Step 3. 클러스터에 스토리지 생성하기

클러스터에 스토리지를 할당하기 위해 서는 스토리지 생성 화면으로 이동합니다.

메뉴이동: ⓦ 플랫폼 관리 &gt; ←클러스터 &gt; \(클러스터 선택\) &gt; ↑스토리지 &gt; 스토리지 목록 &gt; +생성 &gt; 스토리지 생성 화면

스토리지 생성을 위해 유형을 선택합니다. 공통의 환경에서는 NFS 와 NFS Named 유형이 제공되며, Azure 서비스는 Azure Disk 와 Azure File 유형을 추가로 제공합니다.

선택한 유형에 따라 스토리지 생성을 위한 상세 설정이 가능하며, 설정 가능한 정보\(스펙\)는 아래와 같습니다.

> * 이름 \(스토리지 이름\)
> * 설명 \(스토리지 사용자 설명\)
> * 기본 스토리지 \(기본 스토리지 사용여부 선택\)
> * 정책 \(스토리지 삭제 시 정책 설정, Retain or Delete\)
> * 총용량 \(스토리지 총용량, Gb\)
> * 프로비저너 \(스토리지 프로비저닝 값 입력\)
> * 라벨 \(스토리지 라벨 설정\)
> * 주석 \(스토리지 주석 설정\)

Step 4. 파드 보안 설정

클러스터 레벨에서 보안 측면을 제어하기 위해 파드 시큐리티 폴리시를 사용하면 파드 생성 및 업데이트에 대한 세분화된 권한을 부여 할 수 있습니다.

미리 준비된 설정 필드들을 통해 시스템에 적용하기위한 기본값뿐만 아니라 시스템에 적용하기 위해 파드가 실행해야만 하는 조건 셋을 정의 할 수 있으며, 관리자는 아래와 같은 기능을 제어 할 수 있습니다.

제어 가능한 Pod Security 주요 기능

> * 특권을 가진\(privileged\) 컨테이너의 실행 [privileged](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 호스트 네임스페이스의 사용 [hostPID, hostIPC](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 호스트 네트워킹과 포트의 사용 [hostNetwork, hostPorts](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 볼륨 유형의 사용 [volumes](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 호스트 파일시스템의 사용 [allowedHostPaths](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 특정 FlexVolume 드라이버의 허용 [allowedFlexVolumes](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 파드 볼륨을 소유한 FSGroup 할당 [fsGroup](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 읽기 전용 루트 파일시스템 사용 필요 [readOnlyRootFilesystem](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 컨테이너의 사용자 및 그룹 ID [runAsUser, runAsGroup, supplementalGroups](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 루트 특권으로의 에스컬레이션 제한 [allowPrivilegeEscalation, defaultAllowPrivilegeEscalation](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 리눅스 기능 [defaultAddCapabilities, requiredDropCapabilities, allowedCapabilities](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 컨테이너의 SELinux 컨텍스트 [seLinux](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 컨테이너에 허용된 Proc 마운트 유형 [allowedProcMountTypes](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 컨테이너가 사용하는 AppArmor 프로파일 [어노테이션](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 컨테이너가 사용하는 seccomp 프로파일 [어노테이션](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/) 
> * 컨테이너가 사용하는 sysctl 프로파일 [forbiddenSysctls,allowedUnsafeSysctls](https://kubernetes.io/ko/docs/concepts/policy/pod-security-policy/)

## 애플리케이션의 배포 현황은 어떻게 확인 할 수 있나요?

칵테일클라우드에서 배포한 애플리케이션은 워크로드 단위로 배포 되며, 배포 현황에서 확인 가능합니다.  
메뉴 이동 : ⓦ 플랫폼 관리 &gt; ←클러스터 &gt; \(클러스터 선택\) &gt; ↑배포 현황 &gt; 워크로드 목록 화면

배포한 애플리케이션의 배포 상태를 포함하여 워크로드 이름, 워크로드 상태, 배포 유형\(Deployment, Daemon Set, Stateful Set, Job, Cron Job\), 인스턴스 갯수, 현재 자원 사용량\(CPU, Memory\) 배포 후 서비스 Uptime\(Age\) 등을 확인 할 수 있습니다.

![\[&#xD654;&#xBA74;\] &#xC560;&#xD50C;&#xB9AC;&#xCF00;&#xC774;&#xC158; &#xBC30;&#xD3EC; &#xD604;&#xD669; &#xC870;&#xD68C;](../.gitbook/assets/2020-10-20-11.46.11.png)

## 클러스터에서 발생한 알림\(Alert\) 은 어떤 의미 인가요?

운영중인 워크로드 \(혹은 인스턴스\)에서 알림이 발생 할 경우, SMS\(Slack 등\), E-mail, 대시보드를 통해 실시간으로 현황을 제공합니다.

메뉴이동 : ⓦ 플랫폼 관리 &gt; ←클러스터 &gt; \(클러스터 선택\) &gt; ↑알림 &gt; 알림 목록 화면

알림 목록을 통해 해결되지 않은 알림들이 출력되며, 각 알림들은 알림명\(상태 요약\). 중요도\(Critical, Warning\), 발생 일시가 제공됩니다.

![\[&#xD654;&#xBA74;\] &#xD074;&#xB7EC;&#xC2A4;&#xD130; &#xBC1C;&#xC0DD; &#xC54C;&#xB9BC; &#xBAA9;&#xB85D;](../.gitbook/assets/2020-10-20-11.48.09.png)

알림의 상세 정보를 확인하기 위해 알림명을 선택하면, 알림 상세 정보 팝업을 통해 추가정보가 제공됩니다. 

![\[&#xD654;&#xBA74;\] &#xD074;&#xB7EC;&#xC2A4;&#xD130; &#xC54C;&#xB9BC; &#xC0C1;&#xC138; &#xC815;&#xBCF4;](../.gitbook/assets/2020-10-20-11.51.44.png)

## 애드온은 어떤 역할을 하나요?

칵테일 클라우드에서 애드온은 클러스터 운영에 편의를 제공하는 프로메테우스를 포함한 클러스터 매니지먼트 컴포넌트는 애드온 매니저 기능으로 등록/삭제/롤백/재 배포 가능합니다. 사용자 요구애드온 수집/보관 매트릭 대상을 추가/수정 할 수 있습니다. 

1. 모니터링 애드온 수정 
   1. CPU / MEM 등의 상태 및 자원 등의 매트릭 대상 사용자 지정 
   2. 매트릭 임계치 및 최대 / 최소치 사용자 지정 
   3. 지정된 수치에 따라 이벤트 및 알람 발생 
   4. 애드온 버전에 따른 개별 모니터링 매트릭 지정
2. 수정된 매트릭 배포
   1. 수정된 매트릭 정보 \(Rule, Config\) 를 ETCD 저장
   2. 수정된 사용자 정보에 따라 애드온 등록/삭제/롤백/ 재 배포 기능 제공

## 구성 된 클러스터에 스토리지를 증설 한 경우

저장 공간 부족하거나 계획한 작업에 따라 스토리지를 증설 한 경우, 이미 배포되어 있는 Pod 는 증설된 스토리지 정보를 확인 할 수 없습니다. 증설된 스토리지를 정상적으로 사용하기 위해서는 \(증설 전\) 배포 된 Pod 들을 재시작 해야 합니다.

메뉴이동: ←서비스 맵 &gt; ↑서비스 맵 &gt; ▤ \(서비스맵 선택\) &gt; ↑워크로드 &gt; ▤\( 워크로그 선택\) &gt; ▣ 워크로드 상세 &gt; 재시작 선택

![\[&#xD654;&#xBA74;\] &#xD074;&#xB7EC;&#xC2A4;&#xD130; &#xC2A4;&#xD1A0;&#xB9AC;&#xC9C0; &#xC99D;&#xC124; &#xD6C4; &#xC124;&#xC815;](../.gitbook/assets/2020-10-20-12.53.57.png)

