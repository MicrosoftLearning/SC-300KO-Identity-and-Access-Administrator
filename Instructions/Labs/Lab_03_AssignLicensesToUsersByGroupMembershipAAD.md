---
lab:
    title: '03 - 그룹 구성원 자격을 사용하여 라이선스 할당'
    learning path: '01'
    module: '모듈 02 - ID 생성, 구성 및 관리'
---

# 랩 03: 그룹 구성원 자격을 사용하여 라이선스 할당

## 랩 시나리오

조직에서 Azure AD의 보안 그룹을 사용하여 라이선스를 관리하기로 결정했습니다. 새로운 보안 그룹을 구성하고, 해당 그룹에 라이선스를 할당하고, 그룹 구성원 라이선스가 업데이트되었는지 확인해야 합니다.

#### 예상 시간: 10분

## Azure Active Directory에서 새 사용자 생성

1. [https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Overview]( https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Overview)로 이동하고 전역 관리자 권한으로 로그인합니다.

1. 왼쪽 탐색 영역의 **관리**에서 **사용자**를 선택합니다.

1. 사용자 블레이드의 메뉴에서 **새 사용자**를 선택합니다.

1. 다음 정보를 사용하여 사용자를 생성합니다.

    | **설정**| **값**|
    | :--- | :--- |
    | 사용자 이름| Chris|
    | 이름| 크리스 그린(Chris Green)|
    | 이름| Chris|
    | 성| Green|
    | 암호| Pass@word1|

1. 완료되면 **모든 사용자** 목록에 Chris Green의 계정이 표시되는지 확인합니다.

## Azure Active Directory에서 보안 그룹 생성

1. [https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Overview]( https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Overview)로 이동합니다.

1. 왼쪽 탐색 영역의 **관리**에서 **그룹**을 선택합니다.

1. 그룹 블레이드의 메뉴에서 **새 그룹**을 선택합니다.

1. 다음 정보를 사용하여 그룹을 생성합니다.

    | **설정**| **값**|
    | :--- | :--- |
    | 그룹 유형| 보안|
    | 그룹 이름| 마케팅|
    | `구성원 자격 유형| 할당됨|
    | 소유자| *자신의 관리자 계정을 그룹 소유자로 할당*|
    | 구성원| 크리스 그린(Chris Green)|

    ![그룹 유형, 그룹 이름, 소유자 및 구성원이 강조 표시된 새 그룹 블레이드를 보여주는 화면 이미지](./media/lp1-mod2-create-group.png)

1. 완료되면 **Marketing**이라는 그룹이 **모든 그룹** 목록에 표시되는지 확인합니다.

## 그룹에 라이선스 할당

1. **모든 그룹** 목록에서 **Marketing**을 선택합니다.

1. Marketing 블레이드의 **관리**에서 **라이선스**를 선택합니다.

1. 메뉴에서 **할당**을 선택합니다.

1. 라이선스 할당 업데이트 블레이드의 **라이선스 선택**에서 사용 가능한 라이선스 목록을 검토한 후 라이선스 중 하나의 확인란을 선택합니다.

1. **라이선스 검토 옵션**에서 선택한 라이선스에 대해 사용 가능한 옵션을 검토합니다.

    >[!팁]
    >여러 라이선스를 선택한 경우 라이선스 옵션 검토 메뉴를 사용하여 특정 라이선스를 선택하고 해당 라이선스에 대한 라이선스 옵션을 볼 수 있습니다.

    ![선택된 라이선스와 그룹에 할당된 라이선스를 보여주는 화면 이미지. 여러 선택 옵션을 표시하는 라이선스 검토 메뉴도 선택되어 있습니다.](./media/lp1-mod2-assign-license-group.png)

1. **저장**을 선택합니다.
