# dataspell_aesthetic
crt-green — a phosphor terminal theme for dataspell / intellij

crt-green is a custom ide theme + editor color scheme for jetbrains ides (tested primarily in dataspell) inspired by classic green-phosphor crt terminals.

the goal is not “neon hacker green”, but a dim, readable, cohesive look that keeps:
	•	notebooks
	•	editor
	•	terminal
	•	python console

on the same visual surface.

⸻

screenshots

(optional — add later)
notebooks + python console + terminal side by side

⸻

features
	•	dark “crt glass” background (#050806)
	•	phosphor green foreground with muted accents
	•	unified colors across:
	•	editor
	•	jupyter notebooks
	•	run / debug python console
	•	terminal (including ansi palette)
	•	no absolute paths or machine-specific config
	•	pure intellij platform theme (no hacks, no external plugins)

⸻

repository layout

.
├── src
│   └── main
│       └── resources
│           ├── META-INF
│           │   └── plugin.xml
│           └── themes
│               ├── crt-green.theme.json
│               └── crt-green.icls
├── build.gradle.kts
├── settings.gradle.kts
└── README.md


⸻

building the plugin

from the repo root:

./gradlew clean buildPlugin

the plugin zip will be created in:

build/distributions/


⸻

installing in dataspell / intellij
	1.	open settings → plugins
	2.	click the ⚙️ icon → install plugin from disk…
	3.	select the generated .zip
	4.	restart the ide

after restart:
	•	settings → appearance & behavior → appearance
	•	set theme to crt-green
	•	settings → editor → color scheme
	•	set scheme to crt green terminal

for best results:
	•	settings → tools → terminal
	•	enable use ide color scheme

⸻

compatibility
	•	tested with recent dataspell builds (2024–2025)
	•	should work in other jetbrains ides that support custom themes
	•	no os-specific dependencies (mac / linux / windows)

⸻

known limitations

jetbrains renders some components via separate paint paths, so:
	•	a few ui elements may require additional keys depending on ide version
	•	notebooks and consoles are especially version-sensitive

the theme uses broad key coverage to minimize this, but absolute perfection across all builds isn’t guaranteed.

⸻

development notes
	•	.theme.json must be valid json (no comments)
	•	the name field must match the filename prefix
	•	all ui keys live under "ui"
	•	editor syntax is controlled via the .icls scheme

⸻

license

do whatever you want with it.

⸻

motivation

dark terminals are easier on the eyes at 2am, and green phosphor never stopped being correct.
