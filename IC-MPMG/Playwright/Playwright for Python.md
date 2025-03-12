Plugin da biblioteca PyTest, permite escrever [[Testes de Sistema]].
Provê isolamento de contexto, podendo rodar em diferentes browsers.

Arquivos e funções devem seguir a convenção de prefixo do PyTest:
- `test_example.py`
- `def test_has_title()`

Por padrão, os testes são rodados no Chromium, com a opção headless (sem UI).
Comando:
`pytest`
Logs são mostrados no terminal.

----
## Codegen
O comando:
`playwright codegen url`

Abre uma janela do browser e uma tela que gera código a partir das ações executadas na janela. Existem botões para criar assertions e coletar o nome de um elemento html.

----
## Argumentos adicionais:

[Documentação](https://playwright.dev/python/docs/test-runners#cli-arguments)

Os argumentos podem ser especificados automaticamente no pytest.ini:

```ini
# content of pytest.ini
[pytest]
# Run firefox with UI
addopts = --headed --browser firefox
```

Argumentos disponíveis:

- `--headed`: Rodar testes com GUI (default: headless).
- `--browser`: Seleciona o browser a executar os testes `chromium`, `firefox`, or `webkit`. Pode ser definido múltiplas vezes para mais de um browser (default: `chromium`).
- `--browser-channel` Permite executar em browsers de marca. (O PlayWright não os instala por padrão) Opções: `chrome`, `msedge`, `chrome-beta`, `msedge-beta` or `msedge-dev`.
- `--slowmo` Retarda o Playwright pela quantia de tempo especificada em ms. Útil para visualizar suas ações (default: 0).
- `--device` Tipo de dispositivo emulado (tablet, celular, desktop)
- `--output` Diretório para resultados gerados pelo teste (default: `test-results`).
- `--tracing` Quando guardar informações do teste. `on`, `off`, or `retain-on-failure` (default: `off`).
- `--video` Quando gravar um vídeo do teste. `on`, `off`, or `retain-on-failure` (default: `off`).
- `--screenshot` Quando tirar screenshot do teste `on`, `off`, or `only-on-failure` (default: `off`).
- `--full-page-screenshot` Whether to take a full page screenshot on failure. By default, only the viewport is captured. Requires `--screenshot` to be enabled (default: `off`).
- `--color-scheme` Define o tema do browser. (`dark`, `light`).
