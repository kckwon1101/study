# vRealize Log Insight
(*VMware vRealize Log Insight: Deploy and Manage 2019.05.29 강훈 강사님*)
<hr/>

**교육 전 준비**:

교육 내용 : 개념 전달 / 실 사용 위해서는 Docs 확인할 것 / 

Log Insight와 Integration하는 제품들 간의 호환성 이슈/ Proc, API 가이드 참조하기

VMware Communities : http://communities.vmware.com
vRealize Log Insgight Communiti 도 따로 있음

https://vmware.com/education에서 교육 마무리 및 수료증 발급

접속 : 
(터미널 서버 게이트웨이 접속.)
Using the VMware VDC 파일 참조

(토폴로지 그림 중)ESXi 자체 로그 뿐만 아니라 여기에 있는 가상시스템의 로그들도 뽑아낸다??

가상환경 접속 후 ping 으로 각 ip 접속되는지 확인

분석할 사이트의
사이트 Domain Name : vclass.local
인증 도메인 : administrator@vsphere.local(ID)
ping으로 V

처음 원격에서 비번만 VMware1$
나머지는 다 VMware1!

--------------------
## Module 2
로그 정보는 비정형화 데이터(unstructed)
정형화시키고
검색될 수 있도록 분석하고 가시성 있도록 조정 > 이것이 log insight
log insight는 Cloud Management Platform  단이다. 

물리적 장비 : Compute, Network, Storage
로그를 얻으려면 추상화/가상화를 해야 해
compute > ESXi, vCS
network > NSX-V(ESXi), NSX-T(ESXi, KVM) : V에서 T로 옮겨가는 중, KVM기반 컨테이터를 이용한 가상화
storage > vSAN

추상화/가상화를 통해 소프트웨어로 관리가 가능하다. : 아래 기능 모아놓은 것이 vRealize Suite
>제어를 위해 자동화가 되어야 한다 : vR Automation
>모니터링이 필요하다. : vR Operation(운영, 모니터링)
>자원측정이 필요하다. 과금이 가능해진다. : vR (Metering>Cost)
>가시성을 제공해줘야 한다. : vR Network Insight(Visualization)
>로그 정보를 분석할 수 있어야 한다. : vR Log Insight


특징24p : 
1. 전체성에 대한 가능성
2. 정형화 : 내 제품은 정형화하는 방식이 있다. 타 벤터에서 주는 로그데이터는 정형화된 틀(contents pack)로 받으면 된다.(로그인사이트는 카산드라DB를 사용), 제공되지 아니한 데이터는 머신러닝으로 분류(머신러닝에 의한 Smart Field 생성)
3. SDDC와 잘 맞다.
4. 통합관리가 가능
5. 확장이 쉽다.
6. 적절한 가격 제공
+ 25p

gui로만은 한계가 있고 Regex가 필수



