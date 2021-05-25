---
lab:
    title: '21 - 앱 등록 관리에 대한 액세스 권한을 부여하는 새 사용자 지정 역할 만들기'
    learning path: '03'
    module: '모듈 01 - SSO를 위한 엔터프라이즈 앱 통합 계획 및 설계'
---

# 랩 21 - 앱 등록 관리에 대한 액세스 권한을 부여하는 새 사용자 지정 역할 만들기

## 랩 시나리오

앱 관리를 위한 새로운 사용자 지정 역할을 만들어야 합니다. 이 새로운 역할은 자격 증명 관리를 수행하는 데 필요한 특정 권한에만 제한되어야 합니다.

#### 예상 시간: 5분

## 앱 등록 관리에 대한 액세스 권한을 부여하는 새 사용자 지정 역할 만들기

1. 전역 관리자 계정을 사용하여 [https://portal.azure.com](https://portal.azure.com)에 로그인합니다.

1. 포털 메뉴를 열고 **Azure Active Directory**를 선택합니다.

1. Azure Active Directory 블레이드의 **관리**에서 **역할 및 관리자**를 선택합니다.

1. 역할 및 관리자 블레이드의 메뉴에서 **새 사용자 지정 역할**을 선택합니다.

    ![새 사용자 지정 역할 메뉴 옵션이 강조 표시된 역할 및 관리자 블레이드를 표시하는 화면 이미지](./media/lp3-mod1-new-custom-role.png)

1. 새 사용자 지정 역할 블레이드의 기본 정보 탭에 있는 이름 상자에 **내 사용자 지정 앱 역할**을 입력합니다.

1. 나머지 옵션을 검토하고 **다음**을 선택합니다.

1. 사용 권한 탭에서 사용 가능한 권한을 검토합니다.

1. **권한 이름 또는 설명으로 검색** 상자에 **자격 증명**을 입력합니다.

1. 결과에서 **관리** 권한을 선택하고 **다음**을 선택합니다.

    ![검색, 사용 권한 관리, 다음 강조 표시를 포함하는 새 사용자 지정 역할 사용 권한 탭을 표시하는 화면 이미지](./media/lp3-mod1-custom-role-permissions.png)

1. 변경을 검토한 후 **생성**을 선택합니다.