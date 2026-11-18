# experiments — PC 기술 검증 실험

Android 앱에 넣기 전에, PC에서 Python으로 의미 검색 모델(MobileCLIP 등)의 정확도를 먼저 확인하는 폴더입니다. 결과는 [docs/기술검증.md](../docs/기술검증.md)에 기록합니다.

## 데이터셋 구성

```
experiments/
└─ data/              # ⚠️ git에 올리지 않음 (.gitignore)
   ├─ photos/         # 평가용 사진 100장
   └─ queries.csv     # 정답이 표시된 검색어 20개
```

**queries.csv 형식 (예시)**

```csv
query,answers
바닷가에서 본 노을,IMG_0012.jpg;IMG_0045.jpg
카페 영수증,IMG_0101.jpg
```

- `query`: 검색어 (한국어)
- `answers`: 정답 사진 파일명, 여러 장이면 `;`로 구분

## 규칙

- **개인 사진은 커밋하지 않는다.** `experiments/data/`는 `.gitignore`에 등록되어 있다.
- 실험 코드와 결과 요약만 커밋한다.
