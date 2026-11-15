# Kill Human Slop

사람이 만든 디자인을 평범한 AI가 자기 취향대로 바꾸는 스킬입니다.

보라색 그라데이션, 큰 헤드라인, 둥근 카드, 알약 모양 버튼, 부드러운 그림자, 반듯한 그리드. AI가 자연스럽게 고르는 익숙한 스타일로 기존 디자인을 다시 만듭니다.

## 설치

Codex용 사용자 스킬로 설치하려면 GitHub CLI에 로그인한 뒤 실행하세요.

```bash
mkdir -p ~/.agents/skills
gh repo clone Helloworld0822/kill-human-slop ~/.agents/skills/kill-human-slop
```

이미 저장소를 내려받았다면, 저장소 폴더를 `~/.agents/skills/kill-human-slop`에 복사하거나 심볼릭 링크로 연결해도 됩니다. 같은 이름의 폴더가 있으면 덮어쓰지 말고 기존 설치를 먼저 확인하세요.

설치 경로와 심볼릭 링크 지원은 [OpenAI 공식 스킬 문서](https://learn.chatgpt.com/docs/build-skills)를 참고하세요. 설치 후 목록에 나타나지 않으면 Codex를 다시 시작하세요.

## 사용

수정할 프로젝트에서 대상 페이지, 파일 또는 이미지를 지정하고 요청하세요.

```text
$kill-human-slop 이 랜딩 페이지를 네가 좋아하는 스타일로 바꿔줘.
```

```text
$kill-human-slop src/pages/Dashboard.tsx를 평범한 AI 취향으로 다시 디자인해줘.
```

```text
$kill-human-slop 첨부한 포스터를 네 스타일로 바꿔줘.
```

AI가 시각적 방향을 정하고 실제 코드, 편집 가능한 디자인 또는 이미지를 수정합니다. 이미지나 디자인 문서를 수정하려면 해당 형식을 편집할 수 있는 도구가 실행 환경에 있어야 합니다.

## 동작 범위

- 레이아웃, 색상, 타이포그래피, 카드, 버튼과 장식을 바꿉니다.
- 기존 내용, 언어, 링크, 기능, 필수 브랜드 자산과 접근성을 유지합니다.
- 대시보드에는 대시보드에 맞는 스타일을 적용하고, 없는 후기나 수치, 기능을 만들어 넣지 않습니다.
- 변경 결과를 확인하고 실제로 검증한 범위를 알립니다.

스킬 본문은 [SKILL.md](SKILL.md), Codex 표시 정보는 [agents/openai.yaml](agents/openai.yaml)에 있습니다. 별도 실행 코드나 필수 패키지는 없습니다.
