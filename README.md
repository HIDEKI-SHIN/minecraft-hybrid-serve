# 🎮 Minecraft Cross-Version Dedicated Server

Este é um projeto de configuração e otimização de um servidor dedicado de Minecraft focado em alta performance e retrocompatibilidade de protocolos de rede. O ecossistema foi projetado para permitir que clientes de múltiplas versões joguem juntos de forma transparente.

## 🛠️ Tecnologias e Ferramentas
* **Engine Core:** PaperMC (Spigot/Bukkit API) - Escolhido pela otimização extrema de ticks e gerenciamento assíncrono de chunks.
* **Ambiente de Execução:** Java Virtual Machine (OpenJDK).
* **Sistema Operacional de Desenvolvimento:** Linux (CachyOS / Arch Linux).

## 🚀 Arquitetura de Rede e Plugins
O servidor conta com uma esteira de manipulação de pacotes de rede para aceitar conexões híbridas:
* **ViaVersion:** Permite que clientes em versões mais recentes do Minecraft se conectem nativamente no servidor.
* **ViaBackwards:** Garante a retrocompatibilidade, traduzindo pacotes de blocos e entidades novas para que jogadores em versões antigas do cliente consigam renderizar o mundo sem crashes.
* **Spark:** Motor de profiling integrado para monitoramento de consumo de memória Heap, performance de CPU e análise de Thread Locks em tempo real.

## ⚙️ Como Executar Localmente
1. Certifique-se de ter o Java (versão compatível com o core do server) instalado no seu sistema.
2. Clone este repositório.
3. Execute o binário do servidor alocando as flags de memória ideais para a JVM:
   ```bash
   java -Xms2G -Xmx4G -jar server.jar nogui
