- Instalação do Miniconda
	- Versão de CLI disponível no site é mais simples
	- Já seta o PATH, e instala em /home
- Criação do ambiente:
	`conda create --name env1 python=3.10
	`conda activate env1`
- Instalar pytest e playwright via **conda** ou **pip**
	- Via conda precisa de configurar os channels microsoft e conda-forge
	- `playwright install` para instalar os browsers
	- `playwright install --with-deps webkit` se der problema com as dependencias 
- Vscode:
	- Instalar extensão Python
	- Python: Conda Path (user)
	- Python: Default Interpreter Path (workspace/environment)

- Conda não definir environment automaticamente
### Uso e CLI
[[Playwright for Python]]