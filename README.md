# browser-check

A Claude Code plugin that lets Claude open a page in ego lite, a Chromium browser kept for agents, and check it itself: the screen, console errors, failed requests and every request the page sent. It works in Claude Code from any editor or terminal.

This repository only lists the plugin. Its files live in [comonetso/claudeStateBar](https://github.com/comonetso/claudeStateBar/tree/main/skills/browser_check), and installing from here fetches that one folder and nothing else from that repository, so no VS Code extension is installed.

## Install

1. Install [ego lite](https://lite.ego.app/) and sign in there to the sites Claude should check.
2. In Claude Code:

```
/plugin marketplace add comonetso/browser-check
/plugin install browser-check@blueming
```

Then ask Claude to check a page. Node.js 18 or later is needed.

Tested on Windows 11 only: the PC, and Linux servers that use the PC's ego through a relay. It has not been tried on macOS. Clicks and typing happen on the real site, and the write guard has limits; the [plugin README](https://github.com/comonetso/claudeStateBar/blob/main/skills/browser_check/README.md) has the safety rules and the relay setup.

## 한국어

Claude 가 ego lite(에이전트용 크롬 계열 브라우저)로 페이지를 직접 열어 화면·콘솔 오류·실패한 요청·페이지가 보낸 요청을 확인하는 Claude Code 플러그인입니다. 어떤 편집기나 터미널에서 쓰든 Claude Code 만 있으면 됩니다.

이 저장소는 플러그인 목록만 담습니다. 실제 파일은 [comonetso/claudeStateBar](https://github.com/comonetso/claudeStateBar/tree/main/skills/browser_check) 안의 한 폴더에 있고, 여기서 설치하면 그 폴더만 받습니다. VS Code 확장은 설치되지 않습니다.

ego lite 를 설치해 Claude 가 볼 사이트에 로그인해 둔 뒤, Claude Code 안에서 위 두 줄을 입력하면 됩니다. Node.js 18 이상이 필요합니다. Windows 11 에서만 시험했고 macOS 에서는 시험하지 않았습니다. 누르기와 입력은 실제 사이트에서 일어나고 쓰기 차단에도 한계가 있으니, 안전 규칙은 [플러그인 README](https://github.com/comonetso/claudeStateBar/blob/main/skills/browser_check/README.ko.md)를 보세요.

## License

MIT
