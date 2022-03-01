---
lab:
    title: '31 - Azure Active Directory(Azure AD)에서 Microsoft Sentinel로 데이터 연결'
    learning path: '04'
    module: '모듈 04 - Azure Active Directory 모니터링 및 유지 관리'
---

**참고 -- 2월 4일부로 SC-300 랩에서 이 랩의 사용이 중지되었습니다.  조만간 Microsoft Sentinel 관련 작업을 수행하는 더 재미있는 랩이 포함될 예정입니다.  강사는 SC-300 강의 시에 필요에 따라 이 랩을 포함하거나 제외할 수 있습니다.  이 랩을 사용하는 경우 수강생이 Azure Pass와 구독을 설정해야 합니다.**





# 랩 31: Azure Active Directory(Azure AD)에서 Microsoft Sentinel로 데이터 연결

## 랩 시나리오

회사에서 SIEM(Security Information and Event Management) 솔루션을 사용하기 시작할 예정입니다. 즉, 조만간 Microsoft Sentinel 사용이 가능해지므로 Azure AD에 Microsoft Sentinel을 연결하는 방법을 숙지해야 합니다.

#### 예상 시간: 10분

## 사전 요구 사항

- 모든 Azure AD 라이선스(Free/O365/P1/P2)는 Microsoft Sentinel로 로그인 로그를 수집하기에 충분합니다. Azure Monitor(Log Analytics)와 Azure Sentinel에 대해 기가바이트 당 요금이 추가 적용될 수 있습니다.

- 작업 영역에서 사용자에게 Microsoft Sentinel 기여자 역할을 할당해야 합니다.

- 사용자에게 로그를 스트리밍할 테넌트의 전역 관리자 또는 보안 관리자 역할이 할당되어야 합니다.

- 연결 상태를 볼 수 있으려면 사용자에게 Azure AD 진단 설정에 대한 읽기 및 쓰기 권한이 있어야 합니다.

## Microsoft Sentinel 작업 영역 만들기 및 추가

Microsoft Sentinel에 사용할 수 있는 작업 영역이 아직 없는 경우 다음 지침을 사용합니다.

1. 전역 관리자 계정을 사용하여 [https://portal.azure.com](https://portal.azure.com)에 로그인합니다.

2. **Microsoft Sentinel**을 검색하여 선택합니다.

3. Microsoft Sentinel 작업 영역 블레이드의 메뉴에서 **+ 만들기**를 선택합니다.

4. Microsoft Sentinel 작업 영역이 이미 있는 경우 해당 작업 영역을 선택하고 다음 작업을 계속할 수 있습니다.

5. 작업 영역에 Microsoft Sentinel 추가 블레이드에서 **새 작업 영역 만들기**를 선택합니다.

6. 다음 정보를 사용하여 새 로그 분석 작업 영역을 만들 수 있습니다.

    | 설정| 값|
    | :--- | :--- |
    | 구독| 현재의 구독을 사용합니다.|
    | 리소스 그룹| 기존 리소스 그룹을 사용하거나 새 리소스 그룹을 만듭니다.|
    | 이름| **Lab-workspace-yourinitialsanddate**</br>작업 영역은 전역적으로 고유한 값이어야 합니다.|
    | 가격 책정 계층| 종량제(GB당 2018) |

7. **검토 + 만들기**를 선택합니다.
8. **유효성 검사 통과** 메시지가 표시되면 **만들기**를 선택합니다.

9. 완료되면 새 작업 영역을 선택하고 **추가**를 선택하여 Microsoft Sentinel에 작업 영역을 추가합니다.

## Azure Active Directory에 연결

Microsoft Sentinel의 기본 제공 커넥터를 사용하여 [https://docs.microsoft.com/ko-kr/azure/active-directory/fundamentals/active-directory-whatis](https://docs.microsoft.com/ko-kr/azure/active-directory/fundamentals/active-directory-whatis)에서 데이터를 수집한 후Microsoft Sentinel로 스트리밍할 수 있습니다. 커넥터를 사용하여 [https://docs.microsoft.com/ko-kr/azure/active-directory/reports-monitoring/concept-sign-ins](https://docs.microsoft.com/ko-kr/azure/active-directory/reports-monitoring/concept-sign-ins) and [https://docs.microsoft.com/ko-kr/azure/active-directory/reports-monitoring/concept-audit-logs](https://docs.microsoft.com/ko-kr/azure/active-directory/reports-monitoring/concept-audit-logs)를 스트리밍할 수 있습니다.

1. Microsoft Sentinel의 왼쪽 탐색 메뉴에 있는 **구성** 아래에서 **데이터 커넥터**를 선택합니다.

2. **데이터 커넥터** 목록에서 **Azure Active Directory**를 선택한 다음 **커넥터 페이지 열기**를 선택합니다.

    ![Azure Active Directory 커넥터 및 커넥터 열기 페이지가 강조 표시된 데이터 연결선 블레이드를 표시하는 화면 이미지](./media/lp4-mod4-sentinel-add-aad-connector.png)

3. **구성**에서 **Azure Active Directory 로그인 로그** 및 **감사 로그** 체크박스를 선택하고 **변경 내용 적용**을 선택합니다.

    ![Azure Sentinel 선택이 강조 표시된 Azure Active Directory 로그를 표시하는 화면 이미지](./media/lp4-mod4-sentinel-config-aad-connector.png)

4. Microsoft Azure Active Directory 커넥터 페이지를 닫습니다.
