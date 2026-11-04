# Changelog

Every Avenrail release, newest first. Download the latest from the [releases page](https://github.com/ashish200729/avenrail-releases/releases/latest).

## [0.1.1] - 2026-11-04

**See what your agents use, and watch their edits land.** This update adds a Usage page for Claude Code and Codex, and shows file changes as live cards in the chat.

### New

- **Usage.** A new chart button beside Settings shows your cost, tokens and limits.
- **Live edit cards.** See each file change as it happens, with the lines added and removed.

### Usage

- Switch between Cost, Tokens and Limits, over the past 24 hours, 7, 30 or 90 days, or your whole history.
- Cost shows what your usage would cost at standard API list prices, the extra for Fast mode, what caching saved, a daily chart for each provider, and a breakdown by model or by day.
- Cost is an estimate of value, not a bill. Subscriptions are charged differently, and higher rates for very long contexts and hour-long cache writes aren't included.
- Limits shows each signed-in account's plan, how much of its 5-hour, weekly and per-model limits is left, whether you're ahead of pace, and when they reset. For Codex you also see credits, banked resets and lifetime activity.
- Totals are counted from the session logs on your Mac. Once Avenrail has counted a transcript, its totals stay in your history, even after Claude Code deletes it.

### Live edit cards

- When an agent edits or writes a file, the chat shows a card with the file name and the lines added and removed.
- Claude Code, Pi and omp stream an edit while they write it, so the code types itself in as it arrives. With agents that hand over a finished edit, it types in when it lands.
- Once the change has landed, the card rests open a moment and folds to one line. Click it to see the change again, or click the file name to open its diff.
- A patch across several files, or several replacements in one file, shares one card. A very long change says how many lines it leaves out.
- A shell command that only writes files, such as `cat > file <<EOF`, gets a card too. Anything that does more stays a command, so you always see that it will run.

### Also improved

- Token counts read in thousands, millions and billions (K, M, B) in every language setting.
- Subagent rows line up with the other work in the chat.

## [0.1.0] - 2026-11-02

**Avenrail launches.** One calm, native workspace for the coding agents you already use.

### Highlights

- **Every agent, side by side.** Claude Code, Codex, Cursor, Grok Build, OpenCode, Antigravity, Pi, omp, fx and Hermes Agent run in one window, on the subscriptions you already have. Each tab is a session, and panes split right or down so several agents can work at once.
- **A workspace beside every chat.** Files, an editor, Git changes and a terminal sit next to the conversation. Review what an agent changed, commit it, or undo it, without switching apps.
- **Worktrees built in.** Start a session on the current checkout or on a new worktree with its own branch, so parallel work never collides.
- **Orchestration.** An orchestrator session plans the work, hands each part to an agent in its own worktree, and brings the results back together.
- **Operator.** Begin a message with `/operator`, and the agent can open sessions, split panes and sort your sessions into folders for you.
- **PRs & issues.** Pull requests and issues from GitHub, GitLab, Linear and Jira in one inbox, ready to hand to an agent.
- **Automations and reminders.** Run a prompt on a schedule, or when a new issue, pull request or push comes in, and set a reminder on any session.
- **Quick composer.** A global shortcut floats a small composer over whatever app you're in, and starts a session without bringing Avenrail forward.
- **Remote sessions** (experimental). Run agents on an always-on Mac, Linux or Windows machine, and work with them from your desk.

### Made for the Mac

- Native apps for Apple Silicon and Intel Macs.
- Signed automatic updates. Avenrail checks for a new version when it opens and every few hours, and installs one only after you confirm. Every update is verified against Avenrail's signing key first. Running chats are confirmed before the restart and pick up where they left off.
- Before downloading an update, Avenrail tells you if it is running somewhere it can't update itself, such as straight from the disk image.

### Good to know

- Avenrail is not yet notarized by Apple. The first time you open it, choose **Open Anyway** in System Settings › Privacy & Security. Updates never need this step.
- Coming from a preview build? Your conversations, worktrees and settings carry over on first launch, and the preview's own data is left untouched. Install the remote host again on machines you connected to before.
- Windows and Linux builds are coming later.

[0.1.1]: https://github.com/ashish200729/avenrail-releases/releases/tag/v0.1.1
[0.1.0]: https://github.com/ashish200729/avenrail-releases/releases/tag/v0.1.0
