<p align="center"><a href="https://www.iamport.kr"><img src="https://ps.w.org/iamport-payment/assets/banner-772x250.png" width="100%" alt="Iamport Payment"></a></p>

> shortcode를 활용해 아임포트 결제버튼을 어디서든 생성. 신용카드/실시간이체/가상계좌/휴대폰소액결제 가능.

[워드프레스 플러그인 링크](https://wordpress.org/plugins/iamport-payment/)

아임포트는 국내 PG서비스들을 표준화하고 있는 결제 서비스입니다.<br>
아임포트 하나면 국내 여러 PG사들의 결제 기능을 표준화된 동일한 방식으로 사용할 수 있게 됩니다.

이 플러그인은 아임포트 서비스를 어디서든 쉽게 이용할 수 있도록 "결제버튼"을 생성해주는 shortcode를 포함하고 있습니다.<br>
우커머스가 설치되어있지 않은 환경에서도 사용하실 수 있습니다.

`신용카드` / `실시간계좌이체` / `가상계좌` / `휴대폰소액결제`를 지원합니다. <br>
아임포트(https://admin.iamport.kr) 회원가입 후 이용하실 수 있습니다.

http://www.iamport.kr 에서 아임포트 서비스에 대한 보다 상세한 내용을 확인하실 수 있습니다.

데모 페이지 : http://demo.movingcart.kr

*   아임포트 관리자 페이지( https://admin.iamport.kr ) 에서 관리자 회원가입을 합니다.
*   아임포트 플러그인을 다운받아 워드프레스에 설치합니다.
*   아임포트 결제설정 페이지에서 "가맹점 식별코드", "REST API키", "REST API secret"을 플러그인 설정에 저장합니다.


## 설치
> 아임포트 플러그인 설치, https://admin.iamport.kr 에서 관리자 회원가입, 시스템설정 정보저장이 필요합니다.


1. 다운받은 iamport.zip파일을 `/wp-content/plugins/` 디렉토리에 복사합니다.
2. unzip iamport.zip으로 압축 파일을 해제하면 iamport폴더가 생성됩니다.
3. 워드프레스 관리자페이지에서 'Plugins'메뉴를 통해 "아임포트 결제버튼 생성 플러그인" 플러그인을 활성화합니다.
   
![screenshot_1](https://github.com/iamport/wordpress-iamport-pamyent/blob/main/assets/screenshot-1.png)
   
4. https://admin.iamport.kr 에서 관리자 회원가입 후 시스템설정 페이지의 "가맹점 식별코드", "REST API키", "REST API secret"를 확인합니다.
   
![screenshot_2](https://github.com/iamport/wordpress-iamport-pamyent/blob/main/assets/screenshot-2.png)

5. "아임포트 결제설정" 페이지에서 "가맹점 식별코드", "REST API키", "REST API secret" 정보를 저장합니다.

![screenshot_3](https://github.com/iamport/wordpress-iamport-pamyent/blob/main/assets/screenshot-3.png)

6. 워드프레스 관리자페이지 좌측에 생성된 "아임포트 결제설정" 페이지에서 해당 정보를 저장합니다.

## Action Hook

> 아임포트 결제버튼 생성 플러그인이 제공하는 action hook
*   `iamport_button_order_status_changed` : 아임포트 주문데이터의 상태가 변경되었을 때 호출($old\_status, $new\_status, $iamport\_order, $iamport\_api\_response) 4개의 파라메터 제공
    * status
        * ready : 미결제
        * paid : 결제완료
        * failed : 결제실패
        * cancelled : 환불됨
        * awaiting-vbank : 가상계좌 입금대기중
    * iamport\_order : model/iamport-order.php 참조
    * iamport\_api\_response : [아임포트 REST API](https://api.iamport.kr/#!/payments/getPaymentByImpUid) 의 응답필드 참조

## 변경 내역
1.1.19 버전 이후의 패치는 [Github Releases](https://github.com/iamport/wordpress-iamport-payment/releases) 에서 확인해보실 수 있습니다.<br>
과거 변경 내역은 [여기](https://github.com/iamport/wordpress-iamport-payment/blob/master/manuals/VERSION.md) 있습니다.

## FAQ
### 서비스 소개
https://www.iamport.kr
### 관리자 페이지
https://admin.iamport.kr
### 아임포트 docs
https://docs.iamport.kr
### 페이스북
https://www.facebook.com/iamportservice
### 고객센터
1670-5176 / cs@iamport.kr
