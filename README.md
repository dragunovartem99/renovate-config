# renovate-config

Shared [Renovate](https://docs.renovatebot.com) preset for my repos

- Weekly schedule (Monday morning), packages at least 3 days old
- Minor and patch updates grouped into one PR, merged automatically once CI passes
- Major updates stay separate PRs for review
- My own packages (`@dragunovartem99/*`, `html-diagram`, `vue-pgn-viewer`, `99.css`) and
  [pipes](https://github.com/dragunovartem99/pipes) workflows update immediately and merge on green CI
- Lockfile maintenance and `go mod tidy`

## Usage

`renovate.json` in a repo:

```json
{
	"$schema": "https://docs.renovatebot.com/renovate-schema.json",
	"extends": ["github>dragunovartem99/renovate-config"]
}
```

Automerge only happens on repos with CI: Renovate won't merge a PR without passing checks

## License

MIT
