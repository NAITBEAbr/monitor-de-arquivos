# Monitor de arquivos

Fica de olho numa pasta e avisa no terminal sempre que alguma coisa acontece nela:
arquivo criado, alterado, excluído ou movido.

## Como funciona

1. A classe `FileEventHandler` herda de `FileSystemEventHandler` e define o que fazer
   em cada evento: `on_created`, `on_deleted`, `on_modified` e `on_moved`
2. Um `Observer` da biblioteca watchdog vigia a pasta escolhida, incluindo as subpastas
3. Cada evento imprime uma mensagem dizendo qual arquivo mudou
4. O programa roda em laço até você interromper com Ctrl+C

## Tecnologias

- Python
- watchdog

## Como executar

```bash
pip install watchdog
cd PRO-113
python file_system_events_tracker.py
```

Antes de rodar, troque a variável `from_dir` no início do arquivo pela pasta que você
quer monitorar.
