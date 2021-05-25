---
lab:
    title: '07 - 사용자 계정 라이선스 할당 변경'
    learning path: '01'
    module: '모듈 02 - ID 생성, 구성 및 관리'
---

# 랩 07: 사용자 계정 라이선스 할당 변경

## 랩 시나리오

조직 내 일부 사용자 계정에서 할당된 라이선스에 포함된 모든 사용 가능 제품이 제공되지 않거나, 라이선스 할당에 대한 업데이트나 추가가 필요합니다. Azure AD에서 사용자 계정의 라이선스 할당을 업데이트할 수 있는지 확인해야 합니다.

#### 예상 시간: 5분

## Azure Active Directory에서 새 사용자 생성

1. [https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Overview]( https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Overview)로 이동합니다.

1. 왼쪽 탐색 영역의 **관리**에서 **사용자**를 선택합니다.

1. 사용자 블레이드의 메뉴에서 새 사용자를 선택합니다.

1. 다음 정보를 사용하여 사용자를 생성합니다.

    | **설정**| **값**|
    | :--- | :--- |
    | 사용자 이름| Dominique|
    | 이름| Dominique Koch|
    | First name| Dominique|
    | Last name| Koch|
    | 암호| Pass@word1|
    | 사용 위치| *선호하는 사용 위치 선택*|

    >경고
    >사용자에게 라이선스를 할당하려면 사용자에게 사용 위치를 할당해야 합니다.

1. 완료되면 **모든 사용자** 목록에 Chris Green의 계정이 표시되는지 확인합니다.

## 사용자 라이선스 할당 업데이트

1. [https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Overview]( https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Overview)로 이동합니다.

1. 왼쪽 탐색 영역의 **관리**에서 **사용자**를 선택합니다.

1. 사용자 블레이드에서 **Dominique Koch**를 선택합니다.

1. 왼쪽 탐색 영역에서 **라이선스**를 선택합니다.

1. 라이선스 할당 업데이트 블레이드에서 라이선스 하나 이상의 확인란을 선택합니다.

    ![라이선스 할당 업데이트 페이지와 강조 표시된 라이선스 옵션을 보여주는 화면 이미지](./media/lp1-mod2-assign-user-license-options.png)

1. 완료되면 **저장**을 선택합니다.
