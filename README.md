# Blueming's Claude Code plugins

A plugin marketplace for Claude Code. It works in Claude Code from any editor or terminal. Add it once:

```
/plugin marketplace add comonetso/blueming
```

This repository only lists the plugins. Each plugin's files live in its own source repository, and installing one fetches that plugin's folder and nothing else, so no VS Code extension is installed.

## browser-check

Claude opens a page in ego lite, a Chromium browser kept for agents, and checks it itself: the screen, console errors, failed requests and every request the page sent.

1. Install [ego lite](https://lite.ego.app/) and sign in there to the sites Claude should check.
2. In Claude Code, after adding the marketplace above:

```
/plugin install browser-check@blueming
```

Then ask Claude to check a page. Node.js 18 or later is needed.

Tested on Windows 11 only: the PC, and Linux servers that use the PC's ego through a relay. It has not been tried on macOS. Clicks and typing happen on the real site, and the write guard has limits; the [plugin README](https://github.com/comonetso/claudeStateBar/blob/main/skills/browser_check/README.md) has the safety rules and the relay setup. Source: [comonetso/claudeStateBar, skills/browser_check](https://github.com/comonetso/claudeStateBar/tree/main/skills/browser_check).

## codex-rescue

Claude hands a problem it is stuck on, or the code it just changed, to the Codex CLI and takes the answer back without any pasting: an independent investigation of a stuck problem, a review of the changed code, a direct edit by Codex after you confirm, or a short back-and-forth. You can cut in while it runs, ask again about the answer, and every file change it measures is reported.

1. Install the [Codex CLI](https://github.com/openai/codex) and sign in.
2. In Claude Code, after adding the marketplace above:

```
/plugin install codex-rescue@blueming
```

Then say what you want, for example "analyze this with Codex" or "have Codex review the change". Cutting in while it runs needs Node.js 20 or later.

Tested on Windows 11 and on three Linux servers. It has not been run on a real Mac; the shell parts were checked only under a Mac-like shell on Windows. The [guide](https://github.com/comonetso/claudeStateBar/blob/main/docs/codex-rescue-guide.md) explains each mode. Source: [comonetso/claudeStateBar, skills/codex_rescue](https://github.com/comonetso/claudeStateBar/tree/main/skills/codex_rescue).

## 한국어

어떤 편집기나 터미널에서 쓰든 Claude Code 만 있으면 되는 플러그인 목록입니다. 처음 한 번 `/plugin marketplace add comonetso/blueming` 으로 목록을 등록합니다. 이 저장소는 목록만 담고, 플러그인을 설치하면 그 플러그인 폴더만 받습니다. VS Code 확장은 설치되지 않습니다.

**browser-check** — Claude 가 ego lite(에이전트용 크롬 계열 브라우저)로 페이지를 직접 열어 화면·콘솔 오류·실패한 요청·페이지가 보낸 요청을 확인합니다. ego lite 를 설치해 Claude 가 볼 사이트에 로그인해 둔 뒤, 목록을 등록하고 `/plugin install browser-check@blueming` 을 입력하면 됩니다. Node.js 18 이상이 필요합니다. Windows 11 에서만 시험했고 macOS 에서는 시험하지 않았습니다. 누르기와 입력은 실제 사이트에서 일어나고 쓰기 차단에도 한계가 있으니, 안전 규칙은 [플러그인 README](https://github.com/comonetso/claudeStateBar/blob/main/skills/browser_check/README.ko.md)를 보세요.

**codex-rescue** — Claude 가 막힌 문제나 방금 고친 코드를 Codex CLI 에 넘기고 답을 받아 옵니다. 붙여 넣기가 필요 없습니다. 막힌 문제의 독립 조사, 바뀐 코드 리뷰, 확인을 받은 뒤 Codex 가 직접 고치기, 짧은 핑퐁을 할 수 있습니다. 도는 중에 끼어들 수 있고, 답에 다시 물을 수 있으며, 응답 말고 바뀐 파일은 모두 보고합니다. Codex CLI 를 설치해 로그인해 둔 뒤, 목록을 등록하고 `/plugin install codex-rescue@blueming` 을 입력하면 됩니다. 끼어들기에는 Node.js 20 이상이 필요합니다. Windows 11 과 Linux 서버 세 대에서 시험했고 실제 맥에서는 돌려 보지 않았습니다. 모드별 설명은 [가이드](https://github.com/comonetso/claudeStateBar/blob/main/docs/codex-rescue-guide.ko.md)에 있습니다.

## License

MIT
