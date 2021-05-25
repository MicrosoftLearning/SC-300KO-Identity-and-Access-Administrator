---
lab:
    title: '15 - 조건부 액세스 정책 구현 및 테스트'
    learning path: '02'
    module: '모듈 03 - 조건부 액세스 계획, 구현 및 관리'
---

# 랩 15 - 조건부 액세스 정책 구현 및 테스트

## 랩 시나리오

조직에서 내부 애플리케이션에 대한 사용자 액세스를 제한할 수 있어야 합니다. Azure Active Directory 조건부 액세스 정책을 배포해야 합니다.

#### 예상 시간: 10분

## 조건부 액세스 정책 만들기

Azure Active Directory 조건부 액세스는 리소스에 액세스 할 수 있는 사용자를 제어하는 상세 정책을 지정할 수 있는 Azure AD의 고급 기능입니다. 조건부 액세스를 사용하여 그룹, 디바이스 유형, 위치 및 역할과 같은 항목에 따라 사용자의 액세스를 제한하여 애플리케이션을 보호할 수 있습니다.

1. [https://portal.azure.com](https://portal.azure.com)으로 이동한 후 해당 디렉터리에 대한 전역 관리자 계정을 사용하여 로그인합니다.

1. 포털 메뉴를 열고 **Azure Active Directory**를 선택합니다.

1. Azure Active Directory 블레이드의 **관리**에서 **보안**을 선택합니다.

1. 보안 블레이드의 왼쪽 탐색 영역에서 **조건부 액세스**를 선택합니다.

1. 상단 메뉴에서 **새 정책**을 선택합니다.

    ![새 정책이 강조 표시된 조건부 액세스 블레이드를 표시하는 화면 이미지](./media/lp2-mod1-conditional-access-new-policy.png)

1. **이름** 상자에 **Yammer 조건부 액세스**를 입력합니다.

1. 이 연습에서 사용하는 이름이며 원하는 경우 다른 이름을 선택할 수 있습니다.

1. **할당**에서 **사용자 및 그룹**을 선택합니다.

1. 포함 탭에서 **사용자 및 그룹** 확인란을 선택합니다.

1. 선택 창에서 관리자 계정을 선택한 다음 **선택**을 선택합니다.

1. **클라우드 앱 또는 작업**을 선택합니다.

1. **클라우드 앱**이 선택되어 있는지 확인하고 **앱 선택**을 선택합니다.

1. 선택 창에서 **Office 365 Yammer**를 선택하고 **선택**을 선택합니다.

1. **조건**을 선택하고 다시 **조건**을 선택합니다.

1. **구성**에서 **예**를 선택한 다음 **임의의 위치**를 선택합니다.

1. **액세스 제어** 아래에서 **허용**을 선택합니다.

1. 허용 창에서 **액세스 차단**을 선택하고 **선택**을 선택합니다.

    >참고
    >이 정책은 연습에 대해서만 구성되며 조건부 액세스 정책을 신속하게 설명하는 데 사용됩니다.

1. **정책 사용**에서 **켜기**를 선택한 다음, **생성**을 선택합니다.

    ![정책 설정이 강조 표시된 새 조건부 액세스 정책을 표시하는 화면 이미지](./media/lp2-mod3-create-conditional-access-policy.png)

## 조건부 액세스 정책 테스트

조건부 액세스 정책을 테스트하여 예상대로 작동하는지 확인해야 합니다.

1. 새 브라우저 탭을 열고 [https://www.yammer.com/office365](https://www.yammer.com/office365)로 이동합니다.

     자격 증명을 전달해야 합니다.

1. Microsoft Yammer에 액세스할 수 없도록 되어 있는지 확인합니다.

    ![활성화된 조건부 액세스 정책으로 인해 차단된 리소스 액세스가 표시된 화면 이미지](./media/lp2-mod3-test-conditional-access-policy.png)

1. 로그인한 경우 탭을 닫고 1~2분 기다린 후 다시 시도합니다.

1. 탭을 닫고 조건부 액세스 블레이드로 돌아갑니다.

1. **Yammer 조건부 액세스** 정책을 선택합니다.

1. **정책 사용**에서 **끄기**를 선택한 다음, **저장**을 선택합니다.