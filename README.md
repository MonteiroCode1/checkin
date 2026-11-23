# CheckIn Now

Protótipo clicável de um sistema de **chamada digital antifraude**, que registra a presença dos alunos com QR Code dinâmico, localização (GPS) e biometria.

**Protótipo online:** https://monteirocode1.github.io/checkin/index.html

> Este é um protótipo de interface. Tudo o que parece "acontecer" (GPS, biometria, lista de alunos) é simulado para demonstrar o fluxo. Não há servidor, banco de dados nem sensores reais.

---

## Objetivos do sistema

**Objetivo geral:** criar uma chamada digital que impeça fraudes no registro de presença.

**Objetivos específicos**

1. **QR Code dinâmico:** o código exibido no Datashow troca a cada 3 segundos, o que impede o uso de fotos ou prints compartilhados.
2. **GPS e biometria:** o aluno só registra presença se estiver dentro da sala e confirmar sua identidade com a digital.
3. **Painel em tempo real e relatórios:** o professor acompanha as presenças enquanto a aula acontece e consulta a frequência da turma depois.

---

## O que o protótipo mostra

### Visão do professor
- **Chamada ao vivo:** QR Code que se renova a cada 3 segundos, com contagem regressiva.
- **Painel em tempo real:** número de presentes, percentual da turma e lista de presenças com horário.
- **Tentativas bloqueadas:** registro de cada fraude impedida, com o motivo.
- **Relatório:** frequência por aluno, situação (regular ou em risco) e botão de exportar CSV.

### Visão do aluno (celular)
1. Login com matrícula
2. Início com a chamada aberta
3. Escanear o QR Code
4. Verificação de localização
5. Validação por biometria
6. Confirmação de presença, ou tela de erro explicando o motivo

---

## Como usar a demonstração

1. Abra o protótipo no navegador, no computador ou no celular. No celular, use as abas **Professor** e **Aluno**.
2. No celular simulado, clique em **Entrar**, depois em **Registrar presença** e em **Escanear agora**.
3. Aguarde a verificação de localização e toque no ícone de digital.
4. Veja a presença aparecer no **painel do professor**.
5. Use **Simular chegada da turma** para encher a lista de presentes.
6. Abra a aba **Relatório** para ver a frequência e testar a exportação.
7. Clique em **Reiniciar demonstração** para recomeçar.

### Cenários de teste (antifraude)

No bloco **Cenário de teste**, abaixo do celular, escolha antes de escanear:

| Cenário | O que acontece |
|---|---|
| Tudo certo | A presença é registrada normalmente |
| Foto antiga do QR (WhatsApp) | O app informa que o QR expirou e a tentativa aparece no painel |
| Aluno fora da sala | A localização é recusada (simulado a 240 m da sala) |
| Biometria não reconhecida | A digital é recusada e a presença não é registrada |

---

## Tecnologias

- HTML, CSS e JavaScript puros, em um único arquivo (`checkin-now-prototipo.html`)
- QR Code simulado, gerado em SVG a partir de um código que muda a cada 3 segundos
- Fonte Manrope (Google Fonts), com fonte alternativa quando está sem internet
- Tema claro e escuro automático, conforme o dispositivo

## Como abrir o arquivo localmente

1. Baixe `checkin-now-prototipo.html`.
2. Dê dois cliques no arquivo para abrir no navegador. Não precisa instalar nada.

---

## Limitações do protótipo

- O QR Code é visual e não pode ser lido pela câmera de um celular de verdade.
- GPS e biometria são simulados pelos cenários de teste.
- Os dados dos alunos são fictícios e não são salvos ao recarregar a página.

## Próximos passos

- Cadastro de turmas, disciplinas e alunos
- Histórico de presenças do aluno
- Integração real com GPS e biometria do aparelho
- Validação do QR Code no servidor
- Exportação de relatórios em PDF e planilha

---

## Equipe

- _Nome do integrante_ (função)
- _Nome do integrante_ (função)
- _Nome do integrante_ (função)

**Disciplina:** _preencher_
**Professor(a):** _preencher_
**Instituição:** _preencher_
