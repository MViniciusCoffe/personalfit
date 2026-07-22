# PersonalFit: Inteligência de Dados Contra a Evasão em Academias

## 1. Contexto e Objetivos
O **PersonalFit** é um sistema inteligente desenvolvido para otimizar a gestão de academias, focando na retenção de alunos e na eficiência dos instrutores. O projeto surge para resolver um problema crítico do setor: a alta taxa de desistência (evasão), muitas vezes causada pela falta de acompanhamento personalizado e desorganização das prioridades dos professores.

### Objetivos de Estudo:
* **Identificar** os principais motivos de evasão escolar através de relatos reais de usuários.
* **Mapear** as deficiências no atendimento dos instrutores para alimentar o treinamento de uma IA.
* **Validar** as funcionalidades do sistema (como rankings e dashboards) com base nas dores dos alunos.

---

## 2. Curadoria de Fontes
Para este caderno temático, foram selecionadas as seguintes fontes estratégicas presentes no repositório:

* **Transcrição Personalfit (Doc):** Documento base que detalha o modelo de negócio, receita, público-alvo e arquitetura do sistema.
* **Entrevista WhatsApp (18.13.02):** Focada na perspectiva de "ratos de academia" e na sazonalidade dos alunos.
* **Entrevista WhatsApp (18.07.46):** Aborda a toxicidade do ambiente de academia e a importância do "espírito de equipe" e gamificação.
* **Entrevista WhatsApp (18.21.37):** Relata o impacto da situação financeira e do uso de redes sociais (TikTok/YouTube) na motivação inicial.

---

## 3. Engenharia de Prompts e "Cicatrizes"
Nesta seção, documento o processo de extração de conhecimento utilizando o NotebookLM.

* **Prompt Estratégico 1:** *"Quais são os 3 maiores motivos de evasão citados pelos entrevistados?"*
  * **Resultado:** O sistema identificou falta de tempo/rotina, falta de atenção dos instrutores e ambiente desconfortável (som alto/lotação).
* **Prompt Estratégico 2:** *"Como a ideia da transcrição melhora o projeto?"*
  * **Cicatriz (Troubleshooting):** Inicialmente, a IA focou apenas no texto base. Precisei ajustar o prompt para *"cruzar os dados das entrevistas em áudio com a proposta do sistema"*, o que revelou que as transcrições servem como base para treinar a IA de primeira interação.
  * **Aprendizado:** Descobri que a IA tem dificuldade em diferenciar "personal trainer particular" de "instrutor da academia" se não houver um contexto prévio, o que exigiu um refinamento nos prompts de análise.

---

## 4. Miniguia de Estudo (Entrega Final)

### Resumo Estruturado: O Problema da Retenção
A evasão em academias não é apenas física, mas psicológica. Alunos desistem por:

* **Negligência Técnica:** Instrutores que focam em grupos específicos ou não corrigem a mecânica do exercício.
* **Ambiente Hostil:** Som excessivamente alto, falta de empatia no revesamento de máquinas e julgamento alheio.
* **Barreiras de Rotina:** Excesso de responsabilidades (faculdade/trabalho) e falta de um parceiro de treino.

### Glossário de Conceitos Chave

* **Evasão:** Abandono do plano de treinos antes do objetivo ser atingido.
* **Constância:** Capacidade de manter a frequência regular, citada como o maior desafio dos alunos.
* **Mecânica do Exercício:** Execução correta do movimento, essencial para resultados e prevenção de lesões.
* **Gamificação:** Uso de elementos de jogos (como rankings do PersonalFit) para gerar motivação.

### Prompts Reutilizáveis para Revisão

* `"Resuma os pontos negativos do atendimento de instrutores mencionados nas fontes."`
* `"Com base no relato, como a gamificação pode ajudar um aluno que prefere esportes coletivos?"`
* `"Liste os gatilhos de 'virada de chave' que fazem um aluno começar a treinar."`

---
_Este material foi gerado e organizado com o apoio do NotebookLM, utilizando dados reais do projeto PersonalFit._
