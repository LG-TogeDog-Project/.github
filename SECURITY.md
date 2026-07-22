# Security Policy

TogeDog 공개 저장소에는 실제 인증정보를 포함하지 않습니다.

## 공개 금지 항목

- `.env` 및 환경별 비밀 설정
- API key, access token, refresh token, JWT secret, password
- Firebase Admin SDK 서비스 계정 JSON
- `google-services.json`
- `GoogleService-Info.plist`
- 개인 인증서, signing key, keystore
- 비공개 모델 배포 링크 및 내부 네트워크 주소

## 로컬 설정

예시 파일을 복사해 실제 값은 로컬에서만 설정합니다.

```bash
cp .env.example .env
```

학습 노트북의 Roboflow 인증정보는 환경변수로 주입합니다.

```python
import os
os.environ["ROBOFLOW_API_KEY"] = "YOUR_KEY"
```

비밀값이 커밋된 경우 단순 삭제만으로는 충분하지 않습니다. 키를 즉시 폐기·재발급하고 Git 기록에서도 제거해야 합니다.
