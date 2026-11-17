# Optimizer

App de otimização Android que usa o Shizuku para rodar comandos com permissão de shell, sem root.

## Abas
- **Início:** status do Shizuku e ferramentas rápidas
- **Ferramentas:** todas, por categoria (Rápidas, Tela, Apps, Sistema)
- **Ajustes:** como ativar o Shizuku

## Segurança embutida
- Toda entrada é validada por tipo (número, pacote, resolução...) antes de ir ao shell
- Apps essenciais do sistema ficam bloqueados para congelar, forçar parada e remover
- DPI e resolução revertem sozinhos em 10s se não confirmados
- Cada comando tem tempo limite e é encerrado se travar

## Como compilar
Android Studio: abra a pasta e rode. Sem computador: use o GitHub Actions (workflow em `.github/workflows/build.yml` do repositório).

## Estrutura
- `ui/ShizukuManager.kt`: estado, permissão e execução de comandos
- `ui/OptimizerViewModel.kt`: ferramentas, validação, reversão automática
- `ui/OptimizerApp.kt`: telas e diálogos (Jetpack Compose)
