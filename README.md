# Kill Human Slop

사람이 만든 디자인을 평범한 AI가 자기 취향대로 바꾸는 스킬입니다.

보라색 그라데이션, 큰 헤드라인, 둥근 카드, 알약 모양 버튼, 부드러운 그림자, 반듯한 그리드. AI가 자연스럽게 고르는 익숙한 스타일로 기존 디자인을 다시 만듭니다.

## AI에 맞는 형식 선택

| 환경 | 사용할 파일 | 사용 방법 |
| --- | --- | --- |
| ChatGPT, Claude, Gemini 등 일반 채팅 AI | [PROMPT.md](PROMPT.md) | 본문을 채팅에 붙여 넣고 대상 코드나 이미지를 함께 제공 |
| Agent Skills를 지원하는 코딩 AI | [SKILL.md](SKILL.md) | 저장소 폴더를 해당 도구의 스킬 경로에 설치 |

두 파일의 지침은 같습니다. `SKILL.md`에는 검색과 실행을 위한 표준 YAML 메타데이터가 있고, `PROMPT.md`에는 바로 붙여 넣을 본문만 있습니다. 특정 모델이나 MCP, API 키, 추가 패키지는 요구하지 않습니다.

## 일반 채팅에서 사용

1. [PROMPT.md](PROMPT.md)의 전체 본문을 복사해 AI 채팅에 넣습니다.
2. 바꿀 화면의 코드, 이미지 또는 디자인 설명을 함께 제공합니다.
3. 다음처럼 요청합니다.

```text
이 디자인을 네가 좋아하는 평범한 AI 스타일로 바꿔줘.
내용과 기능은 유지하고, 내가 적용할 수정 코드를 보여줘.
```

파일을 직접 편집할 수 있는 AI는 실제 파일을 바꿉니다. 채팅만 가능한 AI는 적용할 코드나 구체적인 재디자인 명세를 반환합니다. 이미지·디자인 파일을 직접 수정하려면 해당 환경에 편집 도구가 있어야 합니다.

## 코딩 AI에 스킬로 설치

공개 저장소이므로 Git으로 바로 내려받을 수 있습니다.

```bash
git clone https://github.com/Helloworld0822/kill-human-slop.git
```

내려받은 `kill-human-slop` 폴더를 사용 중인 도구의 스킬 경로에 복사하세요. 같은 이름의 폴더가 있으면 기존 설치를 먼저 확인하세요.

| 도구 | 사용자 스킬 경로 | 호출 예시 | 공식 문서 |
| --- | --- | --- | --- |
| Codex | `~/.agents/skills/kill-human-slop/` | `$kill-human-slop 이 페이지를 바꿔줘` | [스킬 사용](https://learn.chatgpt.com/docs/build-skills) |
| Claude Code | `~/.claude/skills/kill-human-slop/` | `/kill-human-slop 이 페이지를 바꿔줘` | [스킬 사용](https://code.claude.com/docs/en/skills) |
| Gemini CLI | `~/.agents/skills/kill-human-slop/` 또는 `~/.gemini/skills/kill-human-slop/` | `kill-human-slop 스킬로 이 페이지를 바꿔줘` | [스킬 사용](https://geminicli.com/docs/cli/skills/) |

다른 Agent Skills 지원 도구에서는 해당 도구의 설치 경로를 사용하세요. 스킬을 지원하지 않아도 `PROMPT.md`를 일반 프롬프트로 사용할 수 있습니다. 설치 경로 안내는 위 공식 문서에 근거하며, 모든 도구·모델에서 실행 검증한 것은 아닙니다.

## 동작 범위

- 레이아웃, 색상, 타이포그래피, 카드, 버튼과 장식을 바꿉니다.
- 기존 내용, 언어, 링크, 기능, 필수 브랜드 자산과 접근성을 유지합니다.
- 대시보드에는 대시보드에 맞는 스타일을 적용하고, 없는 후기나 수치, 기능을 만들어 넣지 않습니다.
- 변경 결과를 확인하고 실제로 검증한 범위를 알립니다.

## 파일 구성

- [SKILL.md](SKILL.md): [Agent Skills 표준](https://agentskills.io/specification)에 맞춘 메타데이터와 지침
- [PROMPT.md](PROMPT.md): YAML 메타데이터를 제외한 동일 지침. 일반 채팅용
- [agents/openai.yaml](agents/openai.yaml): Codex의 선택적 표시 정보. 다른 AI에서 사용할 때 필수 파일이 아닙니다.

지침을 수정할 때는 `SKILL.md`의 YAML 아래 본문과 `PROMPT.md`를 동일하게 유지하세요.
