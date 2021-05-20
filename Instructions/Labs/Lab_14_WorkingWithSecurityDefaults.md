---
lab:
    title: '14 - Azure AD Multi-Factor Authentication 사용'
    learning path: '02'
    module: '모듈 03 - 조건부 액세스 계획, 구현 및 관리'
---

# 랩 14 - 보안 기본값 사용

## 랩 시나리오

조직에서 Azure Active Directory 기본 보안 설정을 구성해야 합니다.

#### 예상 시간: 5분

## 보안 기본값 사용

디렉터리에서 보안 기본값을 사용하도록 설정하려면

1. [https://portal.azure.com](https://portal.azure.com)으로 이동한 후 해당 디렉터리에 대한 전역 관리자 계정을 사용하여 로그인합니다.

1. **포털 표시 메뉴** 햄버거 아이콘을 선택하고 **Azure Active Directory**를 선택합니다.

    ![Azure Active Directory가 선택된 Azure Portal 메뉴](./media/azure-portal-menu-aad.png)

1. 왼쪽 창의 관리 섹션에서 **속성**을 선택합니다.

1. 속성 블레이드의 아래쪽에서 **보안 기본값 관리**를 선택합니다.

1. **보안 기본값 사용** 토글을 **예**로 설정합니다.

1. 이는 이미 사용하도록 설정되어 있을 수 있습니다.

1. **저장**을 선택합니다.

### 보안 기본값 사용 안 함

보안 기본값을 대체하는 조건부 액세스 정책을 구현하도록 선택하는 조직은 보안 기본값을 사용하지 않도록 설정해야 합니다.

디렉터리에서 보안 기본값을 사용하지 않도록 설정하려면

1. [https://portal.azure.com](https://portal.azure.com/)으로 이동한 후 해당 디렉터리에 대한 전역 관리자 계정을 사용하여 로그인합니다.

1. **포털 표시 메뉴** 햄버거 아이콘을 선택하고 **Azure Active Directory**를 선택합니다.

1. 속성 블레이드의 아래쪽에서 **보안 기본값 관리**를 선택합니다.

1. **보안 기본값 사용** 토글을 **아니요**로 설정합니다.

    ![보안 기본값을 사용하지 않도록 설정하고 그 근거를 선택하는 화면 이미지. 이 경우, 조직에서 조건부 액세스를 사용하고 있습니다.](./media/security-defaults-disable-before-conditional-access.png)

1. **저장**을 선택합니다.
