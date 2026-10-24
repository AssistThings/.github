# AssistThings

**Tecnologia assistiva aberta, feita com pesquisa.**

AssistThings é um projeto de pesquisa que reúne diversas universidades para criar
tecnologia assistiva **aberta** para apoiar pessoas com deficiência. Trabalhamos
com **Inteligência Artificial** e **Internet das Coisas (IoT)**, sempre com
hardware acessível, processamento local (on-device) e respeito à privacidade.

> Todo o código, os modelos de impressão 3D e a documentação ficam abertos para que
> outras pessoas, laboratórios e comunidades possam reproduzir, adaptar e melhorar.

---

## Projetos

### Smart Glasses: óculos inteligentes para pessoas com deficiência visual

Óculos com câmera USB ligados ao celular. A visão computacional roda no próprio
aparelho, sem enviar nada para a nuvem, e o resultado é falado em voz alta.

| Modo | O que faz |
| --- | --- |
| Ler texto | OCR on-device com leitura estável (sem repetições) |
| Apontar | Lê a linha indicada pela ponta do dedo (MediaPipe Hands) |
| Objetos | Detecta objetos do dia a dia e diz onde estão (esquerda, centro, direita) |
| Cores | Nomeia a cor dominante e diz quando não tem certeza ("parece azul") |
| Rostos | Reconhece pessoas cadastradas, sem guardar fotos |

| Repositório | Descrição | Stack |
| --- | --- | --- |
| [smartglasses-app](https://github.com/AssistThings/smartglasses-app) | App multiplataforma e plugin de câmera UVC (Android validado em hardware real) | Flutter · Kotlin · C (libuvc) · ML Kit · MediaPipe |
| [smartglasses-ios](https://github.com/AssistThings/smartglasses-ios) | App iOS de OCR com câmera ou galeria e histórico local | SwiftUI · Apple Vision |

### Bengala IoT: bengala inteligente

Bengala com sensores ultrassônicos que detectam obstáculos e avisam por vibração, com botão de emergência que envia SMS.

| Repositório | Descrição | Stack |
| --- | --- | --- |
| [bengalaiot-esp32](https://github.com/AssistThings/bengalaiot-esp32) | Dois sensores ultrassônicos, motor de vibração proporcional à distância e BLE. [Simule no Wokwi](https://wokwi.com/projects/360982537270744065) | C++ · ESP32 · BLE |
| [bengalaiot-dragonboard-410c](https://github.com/AssistThings/bengalaiot-dragonboard-410c) | Protótipo original: ultrassom, buzzer e SMS de emergência | Python · mraa · Twilio |
| [bengalaiot-raspberry-pi](https://github.com/AssistThings/bengalaiot-raspberry-pi) | Versão para Raspberry Pi *(em construção)* | — |
| [bengalaiot-android-app](https://github.com/AssistThings/bengalaiot-android-app) | App companheiro Android *(em construção)* | — |
| [bengalaiot-3d-print](https://github.com/AssistThings/bengalaiot-3d-print) | Peças STL: caixa da placa, garra, tampa do sensor, botão de emergência e máscara | STL |

---

## Princípios

- **Aberto:** código, hardware e documentação livres para reproduzir e adaptar.
- **Privacidade:** o processamento acontece no aparelho. Imagens e rostos não vão para a nuvem.
- **Acessível:** usa componentes baratos e fáceis de encontrar (ESP32, câmeras UVC, impressão 3D).
- **Centrado nas pessoas:** as funções vêm de necessidades reais de quem usa.

## Instituições parceiras

- UFSCar, DEPS, Campus Sorocaba (peças de impressão 3D: Prof. Cleyton Fernandes Ferrarini)
- *(adicione aqui as demais universidades e laboratórios)*

## Como contribuir

1. Escolha um repositório e leia o README e a pasta `docs/`.
2. Abra uma *issue* para relatar um problema ou propor uma ideia.
3. Mande um *pull request*. Testes e acessibilidade (leitores de tela, TalkBack, VoiceOver) contam muito.

Pesquisadores, estudantes e pessoas com deficiência que queiram testar os protótipos
são muito bem-vindos.
