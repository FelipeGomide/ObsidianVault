Settings.json:

``` json
{
	"workbench.colorTheme": "Catppuccin Mocha",
	// we try to make semantic highlighting look good
	"editor.semanticHighlighting.enabled": true,
	// prevent VSCode from modifying the terminal colors
	"terminal.integrated.minimumContrastRatio": 1,
	"catppuccin.accentColor": "green",
	
	"catppuccin.customUIColors": {
		"mocha": {
			"statusBar.foreground": "accent",
		},
	},
	
	"catppuccin.workbenchMode": "flat",
	"window.titleBarStyle": "custom",
	"catppuccin.italicKeywords": false,
	"catppuccin.boldKeywords": false,
	
	"editor.minimap.enabled": false,
	"editor.stickyScroll.enabled": false,
	"breadcrumbs.enabled": false,
	"editor.renderControlCharacters": false,
	"editor.renderWhitespace": "none",
	
	"editor.inlayHints.enabled": "off",
	"workbench.layoutControl.enabled": false,
	"workbench.iconTheme": "catppuccin-perfect-mocha",
	"editor.fontFamily": "'Cascadia Code NF'",
	"editor.fontLigatures": "'calt', 'ss01', 'ss19'",
	"terminal.integrated.fontFamily": "Iosevka Term",
	
	"python.condaPath": "~/miniconda3",
	"workbench.productIconTheme": "material-product-icons",
	"workbench.sideBar.location": "right",
	
	"python.terminal.activateEnvironment": false,
}
```