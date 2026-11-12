# 🩺 SaúdeCheck | Sistema Inteligente de Triagem e Geolocalização Médica

**SaúdeCheck** é uma aplicação móvel de nível de produção desenvolvida nativamente em **Kotlin** e **Jetpack Compose**. Concebida para o **Twodio Code Challenge**, a plataforma foca-se em resolver os gargalos da triagem pré-hospitalar e no encaminhamento célere de pacientes para unidades de emergência médica em **Luanda, Angola**.

---

## 🤖 Engenharia Impulsionada por Inteligência Artificial (Google AI Studio)
O desenvolvimento e a arquitetura deste projeto beneficiaram do suporte avançado do **Google AI Studio**. A plataforma foi utilizada estrategicamente para:
- **Conceção de Arquitetura:** Desenho rigoroso dos padrões de Clean Architecture e MVVM aplicados ao ecossistema Android.
- **Otimização de Algoritmos:** Refinamento do motor de triagem em Kotlin para garantir alta performance e baixo consumo de recursos.
- **Documentação e Engenharia de Software:** Estruturação de componentes modulares, testes de concorrência com Coroutines e boas práticas de código limpo.

---

## 🏛️ Arquitetura de Software & Padrões de Projeto
O projeto foi estruturado seguindo rigorosamente os princípios da **Clean Architecture** e do padrão **MVVM (Model-View-ViewModel)**, garantindo modularidade, testabilidade e separação estricta de responsabilidades:

- **Apresentação (UI Layer):** Construída inteiramente com **Jetpack Compose** e **Material Design 3**, utilizando um paradigma declarativo que elimina o acoplamento pesado com views tradicionais. A gestão de estado reativa (`StateFlow` e `MutableStateFlow`) garante uma interface fluida a 60fps sem bloqueio da thread principal.
- **Domínio (Domain Layer):** Contém os casos de uso (*Use Cases*) de negócio puros, isolando as regras de triagem e cálculo de prioridade médica de qualquer dependência externa ou framework de UI.
- **Dados (Data Layer):** Repositórios centralizados que gerem o fluxo de fontes de dados locais (armazenamento persistente) e serviços remotos.

---

## ⚙️ Stack Tecnológica & Ecossistema

| Camada / Componente | Tecnologia Utilizada | Justificativa Técnica |
| :--- | :--- | :--- |
| **Linguagem Principal** | Kotlin (Coroutines & Flow) | Segurança de nulos (*Null Safety*), concorrência assíncrona eficiente e interoperabilidade total com o ecossistema Android. |
| **Interface Gráfica** | Jetpack Compose (Material 3) | Desenvolvimento UI moderno, reativo, menos propenso a erros de estado e com suporte nativo a temas dinâmicos. |
| **Injeção de Dependências** | Hilt / Dagger (ou Gestão Modular) | Desacoplamento de componentes e gestão otimizada do ciclo de vida das instâncias. |
| **Processamento Concorrente** | Kotlin Coroutines & Dispatchers | Execução de tarefas intensivas em background (como algoritmos de triagem) sem congelar a experiência do utilizador. |
| **Ambiente de Build** | Gradle (Kotlin DSL) | Configuração de compilação modularizada, otimizada para builds rápidos e limpos. |

---

## 🚀 Funcionalidades Técnicas Principais

1. **Motor de Triagem Baseado em Regras Clínicas:**
   - Algoritmo em Kotlin que processa inputs sintomatológicos do utilizador em tempo real, calculando scores de gravidade e recomendando o nível de urgência adequado.
2. **Módulo de Mapeamento Hospitalar:**
   - Integração com sistemas de geolocalização para calcular distâncias a centros de saúde e hospitais de referência em Luanda.
3. **Resiliência e Desempenho (Offline-First):**
   - Estrutura de dados pensada para operar com restrições de conectividade, garantindo que os fluxos críticos de triagem funcionem mesmo com sinal instável.

---

## 📦 Distribuição e Testes (APK)
Para facilitar a avaliação prática imediata pelos jurados sem a necessidade de compilar o código fonte no Android Studio, a versão de produção compilada (`.apk`) está disponível para descarregamento direto:

🔗 **[Descarregar o APK Oficial do SaúdeCheck (MediaFire)]([COLOQUE_AQUI_O_LINK_DO_MEDIAFIRE](https://www.mediafire.com/file/61skz6iaqw1sovb/Sa%25C3%25BAdeCheck_1.0.apk/file))**

---

## 🛠️ Como Executar o Projeto Localmente
Caso pretenda auditar o código fonte diretamente no **Android Studio**:

1. Clone o repositório ou descarregue o código fonte em formato ZIP.
2. Abra o **Android Studio** (versão Electric Eel ou superior recomendada).
3. Selecione *File > Open* e aponte para a pasta raiz do projeto (`saúdecheck`).
4. Aguarde a sincronização completa das dependências do **Gradle**.
5. Conecte um dispositivo físico Android ou inicie um *Emulator* (API 24 ou superior).
6. Clique no botão **Run (▶️)** para compilar e executar.

---

## 👨‍💻 Autor & Licenciamento
Desenvolvido por **Mario** com o apoio técnico do **Google AI Studio**, seguindo os padrões de excelência de engenharia de software para o Twodio Code Challenge.
