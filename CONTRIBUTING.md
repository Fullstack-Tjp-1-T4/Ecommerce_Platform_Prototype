# 🤝 협업 규칙

## 🌿 브랜치 전략

| 브랜치 | 용도 |
|---|---|
| `main` | 최종 제출 / 배포용. **직접 push 금지** |
| `develop` | 개발 통합 브랜치. 기능이 완성되면 여기로 merge |
| `feature/기능명` | 기능 개발용 브랜치 |
| `fix/버그명` | 버그 수정용 브랜치 |

**브랜치 이름 예시**
```
feature/product-list
feature/cart
feature/payment
feature/review
fix/cart-total-price
```

<br>

## 🔁 작업 흐름

```bash
# 1. develop 최신화
git checkout develop
git pull origin develop

# 2. 작업 브랜치 생성
git checkout -b feature/기능명

# 3. 작업 후 커밋
git add .
git commit -m "feat: 기능 설명"

# 4. 원격에 push
git push origin feature/기능명

# 5. GitHub에서 develop 브랜치로 Pull Request 생성
```

> ⚠️ PR을 올리기 전에 `develop`을 한 번 더 pull 받아서 충돌이 없는지 확인해 주세요.

<br>

## ✏️ 커밋 메시지 규칙

```
타입: 작업 내용 (한글 OK)
```

| 타입 | 의미 | 예시 |
|---|---|---|
| `feat` | 새로운 기능 추가 | `feat: 장바구니 담기 기능 추가` |
| `fix` | 버그 수정 | `fix: 결제 금액 계산 오류 수정` |
| `docs` | 문서 수정 | `docs: README 실행 방법 추가` |
| `style` | 코드 포맷팅 (기능 변경 없음) | `style: 들여쓰기 정리` |
| `refactor` | 코드 리팩토링 | `refactor: 주문 로직 함수 분리` |
| `test` | 테스트 코드 | `test: 리뷰 등록 테스트 추가` |
| `chore` | 설정, 패키지 등 기타 | `chore: .gitignore 수정` |

<br>

## 🔍 Pull Request 규칙

- PR 제목은 커밋 메시지 규칙과 동일하게 작성합니다. (예: `feat: 상품 목록 페이지 구현`)
- PR 템플릿의 항목을 채워 주세요.
- **팀원 1명 이상 승인(Approve)** 후 merge합니다.
- 관련 이슈가 있으면 본문에 `Closes #이슈번호`를 적어 주세요. merge되면 이슈가 자동으로 닫힙니다.

<br>

## 📝 이슈 규칙

- 작업을 시작하기 전에 이슈를 먼저 만들고 담당자(Assignee)를 지정합니다.
- 라벨을 붙여 주세요: `feature`, `bug`, `frontend`, `backend`, `payment`, `docs`

<br>

## 🚫 주의사항

- `.env`, API 키, 비밀번호 등 **민감한 정보는 절대 커밋하지 않습니다.**
- 다른 사람이 담당한 파일을 수정해야 하면 미리 말해 주세요.
- 하루 작업이 끝나면 push해서 작업 내용이 로컬에만 남지 않게 합니다.
