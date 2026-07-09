# ❄️ HCooling

Aplicativo para Windows que reúne monitoramento de hardware e gerenciamento de perfis de energia em uma interface simples.

[![Última versão](https://img.shields.io/github/v/release/akaharo/HCooling-Installer?label=vers%C3%A3o&color=2ea44f)](https://github.com/akaharo/HCooling-Installer/releases/latest)
![Plataforma](https://img.shields.io/badge/plataforma-Windows%2010%20%7C%2011-0078D6?logo=windows)
![Arquitetura](https://img.shields.io/badge/arquitetura-x64-blue)
![Interface](https://img.shields.io/badge/interface-Electron%20%2B%20JavaScript-47848F?logo=electron)
![Sensores](https://img.shields.io/badge/sensores-C%23%20%2B%20.NET-512BD4?logo=dotnet)

> Este repositório é destinado à distribuição do instalador e das atualizações do HCooling.

## 📥 Download

**[Baixar a versão mais recente](https://github.com/akaharo/HCooling-Installer/releases/latest)**

Na seção **Assets** da release, baixe o arquivo `HCooling.Setup.<versão>.exe`.

## 🖥️ Interface

![Interface do HCooling](./screenshot.png)

## ✨ Recursos

- Temperatura, uso e frequência da CPU e da GPU;
- Uso da memória RAM;
- Histórico de temperaturas, com valores mínimos e máximos;
- Perfis de energia: desempenho máximo, uso padrão e modo frio;
- Inicialização automática com o Windows;
- Execução em segundo plano pela área de notificação;
- Intervalo de atualização dos sensores configurável;
- Verificação e instalação automática de novas versões.

## ✅ Requisitos para executar

| Requisito | Detalhes |
| --- | --- |
| Sistema operacional | Windows 10 ou Windows 11 de 64 bits |
| Arquitetura | Processador e sistema x64 |
| Runtime | Microsoft .NET Framework 4.7.2 ou superior |
| Permissões | Acesso de administrador para leitura dos sensores e aplicação dos perfis de energia |
| Hardware | Sensores compatíveis e expostos pela placa-mãe, CPU e GPU |
| Internet | Necessária para baixar o instalador e receber atualizações automáticas |

O instalador já inclui o Electron, o componente de leitura de sensores e as bibliotecas usadas pelo aplicativo. **Não é necessário instalar Node.js, npm, Electron ou o SDK do .NET manualmente.**

## 🧩 Tecnologias e linguagens

| Camada | Tecnologia | Finalidade |
| --- | --- | --- |
| Interface | HTML5 e CSS3 | Estrutura, tema e componentes visuais |
| Aplicação desktop | JavaScript e Electron 39 | Interface, configurações, integração com o Windows e atualizações |
| Sensores | C# e .NET Framework 4.7.2 | Processo auxiliar responsável pela leitura do hardware |
| Monitoramento | LibreHardwareMonitor, OpenHardwareMonitor e `systeminformation` | Coleta de temperaturas, uso, clocks e informações do sistema |
| Gráficos | Chart.js 4 | Histórico visual das temperaturas |
| Instalador | electron-builder e NSIS | Empacotamento e instalação no Windows |

## 📦 Dependências incluídas

- Electron 39;
- Chart.js 4.5;
- `systeminformation` 5.30;
- HCooling Sensor Host;
- LibreHardwareMonitor e OpenHardwareMonitor;
- Bibliotecas auxiliares necessárias para acesso aos sensores.

## 🚀 Instalação

1. Baixe o instalador na [release mais recente](https://github.com/akaharo/HCooling-Installer/releases/latest).
2. Execute `HCooling.Setup.<versão>.exe`.
3. Escolha a pasta de instalação e conclua o processo.
4. Abra o HCooling pelo atalho criado na área de trabalho.
5. Autorize a execução como administrador quando o Windows solicitar.

## ℹ️ Observações de compatibilidade

- A disponibilidade de cada temperatura depende dos sensores expostos pelo hardware e pelo firmware do computador;
- Em alguns equipamentos, determinados dados podem não estar disponíveis mesmo com permissão de administrador;
- O aplicativo funciona sem internet após a instalação, mas a verificação de atualizações ficará indisponível;
- Caso encontre um problema, abra uma [issue](https://github.com/akaharo/HCooling-Installer/issues) informando a versão do HCooling, a versão do Windows e o hardware utilizado.
