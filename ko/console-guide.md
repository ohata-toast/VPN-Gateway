## Network > VPN Gateway(Site-to-Site VPN) > 콘솔 사용 가이드

#### VPN Gateway 생성

* 이름: 생성할 VPN Gateway의 이름을 입력합니다.
* VPC: VPN Gateway를 만들 VPC를 선택합니다.
* Subnet: VPN Gateway를 만들 subnet을 선택합니다.
* 설명: 필요한 설명을 입력합니다.

#### VPN Gateway 변경

* 이름과 설명을 변경할 수 있습니다.

#### VPN Gateway 삭제

* 선택한 Gateway를 삭제할 수 있습니다.
* 삭제하려면 연결된 VPN Conenction이 없어야 합니다.

#### VPN Connection 생성

* 터널 옵션을 선택하여 VPN Connection을 생성할 수 있습니다.
* VPN Connection이 생성 되는데에는 시간이 수분 정도 걸릴수 있습니다.
* 생성이 완료되면 상태 표시가 `ACTIVE`로 변경 됩니다.

#### VPN 터널 옵션
* 로컬 ipv4 CIDR : VPN 터널을 통한 통신이 허용된 NHN Cloud 측 IPv4 CIDR 범위
  * 선택한 Subnet의 대역이 들어가게 됩니다.
* 리모트 ipv4 CIDR : VPN 터널을 통한 통신이 허용된 고객 게이트웨이(온프레미스)측 IPv4 CIDR 범위
* IKE1 암호화/무결성 알고리즘 : 1단계 IKE 협상에 대해 VPN 터널에 허용되는 암호화, 무결성 알고리즘
  * (aes192, aes256, des, 3des 중 택 1)-(md5, sha1 중 택 1)
* IKE1 인증 수명시간 : 1단계 IKE 협상의 수명(초)입니다.
  * 900에서 28,800 사이의 숫자를 지정할 수 있습니다.
* 1단계 Diffie-Hellman(DH) Group :  IKE 협상의 1단계에서 VPN 터널에 허용되는 DH 그룹 번호입니다.
  * 32, 31, 30, 29, 28, 27, 21, 20, 19, 18, 17, 16, 15, 14, 5, 2, 1 중 택 1
* IKE2 암호화/무결성 알고리즘 : 2단계 IKE 협상에 대해 VPN 터널에 허용되는 암호화, 무결성 알고리즘
  * (aes192, aes256, des, 3des 중 택 1)-(md5, sha1 중 택 1)
* IKE2 인증 수명시간 : 2단계 IKE 협상의 수명(초)입니다.
  * 900에서 28,800 사이의 숫자를 지정할 수 있습니다.
* IKE2 Diffie-Hellman(DH) Group : IKE 협상의 2단계에서 VPN 터널에 허용되는 DH 그룹 번호입니다.
  * 32, 31, 30, 29, 28, 27, 21, 20, 19, 18, 17, 16, 15, 14, 5, 2, 1 중 택 1
* 대역폭 : 연결에 사용할 대역폭을 결정합니다.
  * 20M, 50M, 100M, 1G 중 택1
  * outbound 대역폭을 의미합니다.
* 사전공유키(PSK) : 사전 공유 키(PSK)는 대상 게이트웨이와 고객 게이트웨이 사이의 초기 인터넷 키 교환(IKE) 보안 연결을 설정합니다.
  * 영숫자, 마침표(.), 밑줄(_)을 사용할수 있습니다.
  * 8~64 바이트 사이의 입력값이 필요합니다.

#### VPN Connection 변경

* 이름과 설명을 변경할 수 있습니다.

#### VPN Connection 삭제

* 선택한 VPN Connection을 삭제할 수 있습니다.
