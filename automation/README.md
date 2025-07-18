# 🤖 automation/

⚠️ 본 문서는 개인 포트폴리오용으로 제작된 자료이며, 특정 기업의 실제 데이터나 민감한 정보는 포함되어 있지 않습니다.

- 장바구니 핵심 기능의 테스트 시나리오와 테스트 케이스를 기반으로 작성한 테스트 스크립트입니다.
- Playwright + TypeScript 환경에서 테스트 자동화를 구현하였으며, 테스트 케이스 검증 및 반복 테스트 효율화를 목표로 합니다.

## 📄 **tests/cart_core_functionality_test.spec.ts**

- 글로벌 이커머스 플랫폼의 장바구니 핵심 기능 테스트 케이스를 기반으로 작성된 **Playwright 자동화 테스트 스크립트**입니다.
- 테스트 시나리오 및 테스트 케이스 문서(`../test-cases/`)에서 정의한 항목을 바탕으로 자동화 가능한 항목만 선별하여 구현하였습니다.

### 📝 포함된 테스트 케이스

| TC ID | 테스트 항목 |
|-------|-------------|
| CART_001 | 상품 검색 후 장바구니에 상품 추가 가능 여부 확인|
| CART_002 | 동일 상품 여러 번 추가 시 수량 자동 증가 확인 |
| CART_003 | 장바구니 수량 변경 시 총 금액 갱신 확인 |
| CART_005 | 장바구니 상품 삭제 기능 확인 |

### 📝 제외된 테스트 케이스

| TC ID | 제외 사유 |
|-------|------------|
| CART_004 | 상품 수량 제한 정책 확인 케이스는 실제 테스트 환경 및 데이터 상황에 따라 자동화 구현이 어려움 |

## 📄 **tests/config.ts**

- 테스트의 공통 상수를 관리하는 파일입니다.
- 테스트 환경 또는 URL 변경 시, config.ts 파일만 수정하면 전체 테스트 스크립트에 자동으로 반영되도록 구성하였습니다.

### 📝 포함된 항목

| 변수명 | 설명 |
|--------|------|
| BASE_URL | 테스트 대상 글로벌 이커머스 플랫폼 메인 페이지 URL |
| CART_URL | 장바구니 페이지 URL |

## 📊 자동화 테스트 실행 결과 리포트 예시

- 테스트 실행 결과 리포트는 `playwright-report/` 디렉토리에 HTML 형태로 자동 생성되며, 브라우저로 열어 상세 결과를 확인할 수 있습니다.

| CART_001 | CART_002 |
| ---- | ---- |
| <img width="1440" alt="Image" src="https://github.com/user-attachments/assets/a14d7b04-61c9-4e21-934a-cee5df837de5" /> | <img width="1440" alt="Image" src="https://github.com/user-attachments/assets/ecde3b54-d71c-4694-8114-08c41b55f782" /> |

| CART_003 | CART_005 |
| ---- | ---- |
| <img width="1440" alt="Image" src="https://github.com/user-attachments/assets/427acddc-5188-4517-a953-36c4b0eca77d" /> | <img width="1440" alt="Image" src="https://github.com/user-attachments/assets/77df0abd-f6d0-47f7-9765-24f3f32ed189" /> |

## 🚀 테스트 실행 방법

1. 패키지 설치

```
npm install
```

2. 테스트 실행

```
npx playwright test
```

3. 테스트 리포트 확인

```
npx playwright show-report
```
