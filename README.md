# Kelsca Financial 5.0 · Seu dinheiro, sua estratégia

Uma aplicação de planejamento de tesouraria familiar **100% estática e gratuita**, feita em HTML, CSS e JavaScript sem frameworks, banco de dados, build ou mensalidade de hospedagem. Os dados são preenchidos manualmente no próprio site e armazenados no navegador. O JSON é **apenas uma opção de backup**.

## O que o sistema faz

- **Olho mágico** no canto superior: mostra e oculta valores financeiros em todo o aplicativo (`R$ ••••`), inclusive grade mensal, cartões, formulários e fluxo de caixa. Gráficos sensíveis são desfocados/ocultos. O modo continua ativo entre páginas e recarregamentos, mas não criptografa os dados.
- **Rendas editáveis:** salários, aluguéis, 13º, férias, bônus e dividendos, incluindo ligação opcional da estimativa de dividendos da carteira ao orçamento; receitas são separadas de benefícios como VA/VR.
- **Grade dinâmica dos próximos 12 meses:** altere mês a mês os valores de receitas, despesas e parcelas; gráficos e projeções são atualizados. Valores editados naquele mês prevalecem sobre o valor padrão.
- **Tesouraria e prioridades personalizadas:** informe dinheiro líquido disponível, valor protegido, contas não pagas e a ordem desejada dos próximos objetivos. Reordene com setas ou arrastando, defina tetos e ative/desative cada destino. O app sugere três decisões explicadas; contas essenciais vêm primeiro.
- **Agenda financeira:** dia habitual de recebimento ou vencimento e alteração pontual do dia em cada mês; análise de risco de faltar dinheiro antes da próxima entrada quando o saldo de abertura é informado.
- **Semáforo de contas fixas:** verde = pago, amarelo = vence hoje, vermelho = atrasado, azul = programado. Pagamento deve ser confirmado pelo próprio usuário. Lembretes por arquivo `.ics` (próximos 12 meses) e notificações do navegador **somente com a página aberta e autorização**.
- **WhatsApp manual:** opção de guardar um número localmente e abrir uma mensagem de lembrete pronta para conferência e envio. **Não envia mensagens automaticamente.** Para isso, seria necessária integração com serviço externo e processos de autorização, que podem ter custo.
- **Fluxo de caixa separado D+30, D+60 e D+90:** usa saldo atual e datas de movimentações não confirmadas, mostra risco de saldo negativo ao longo dos próximos 90 dias. Dividendos de data incerta e VA/VR não entram como dinheiro disponível.
- **Cartões e dívidas:** saldo para quitação, soma das parcelas a vencer (quando conhecida), vencimentos, pagamentos reais, comparação de alívio e simulação de quitação. Consignados já descontados do líquido não são debitados duas vezes.
- **Linha do tempo / medalhas / troféus / honras:** conquistas simbólicas quando o usuário registra de fato pagamentos, quitações e aportes nas metas. Simulações não dão prêmios.
- **Metas e sonhos:** reserva de emergência, construir a casa, compras, objetivos familiares, contribuições e prazos.
- **Cofrinhos e investimentos:** simulações do CDI, carteira de ações/FIIs, cotações manuais ou atualização opcional pela brapi (sujeita ao serviço), dividendos estimados e metas de renda.
- **Backup opcional:** exportação e importação de JSON; dados preenchidos persistem automaticamente no `localStorage` daquele navegador.

## Publicar gratuitamente no GitHub Pages

1. Acesse **https://github.com/KDalcantara/Kelsca-Financial**.
2. Na raiz do repositório, envie `index.html`, `styles.css`, `app.js`, `README.md` e `.nojekyll`, substituindo os nomes existentes (ou editando os arquivos antigos).
3. Se ainda não tiver configurado a publicação, abra **Settings → Pages → Deploy from a branch → main → /(root) → Save**.
4. Visite **https://kdalcantara.github.io/Kelsca-Financial/** quando o deployment terminar.

**Não suba o arquivo HTML de teste com dados preenchidos, seus backups ou outras planilhas pessoais**. Este projeto distribuído tem apenas categorias vazias e valores fictícios de demonstração.

## Como usar

1. Abra **Meu saldo atual** e informe o valor líquido existente na conta e a quantia protegida.
2. Em **Fontes de renda**, ajuste o padrão do salário, dos aluguéis etc.; em **Planejar 12 meses**, ajuste meses específicos.
3. Em **Agenda financeira**, informe datas de salário e das contas. Em **Contas e alertas**, acompanhe os vencimentos, configure os lembretes e marque pagamentos efetivamente feitos.
4. Em **Tesouraria e prioridades**, decida a ordem para o dinheiro restante. As contas essenciais são protegidas antes das escolhas opcionais.
5. Em **Fluxo D+30/60/90**, confira períodos de possíveis faltas e adapte o planejamento.
6. Em **Minha jornada**, veja sua evolução após registrar pagamentos e aportes efetivos.
7. Clique no botão de **olho** do topo para ocultar/revelar valores em locais públicos. Faça backups regularmente em **Backup → Exportar JSON**.

## Segurança e limitações

- A aplicação não tem servidor, conta de usuário, envio automático bancário ou armazenamento sincronizado na nuvem. **Cada navegador/dispositivo tem seus próprios dados.** Limpar os dados do navegador pode apagar tudo; exporte backups e guarde-os com segurança.
- O modo privacidade é **apenas uma máscara de exibição**. Não oferece login, bloqueio por senha nem criptografia. Qualquer pessoa com acesso ao navegador e aos dados locais poderá potencialmente revelá-los.
- GitHub Pages publica os arquivos do site para qualquer pessoa, portanto **não coloque valores reais da família nem dados pessoais no repositório**.
- As três decisões e as projeções são **simulações**. A aplicação não executa pagamento, aporte nem pedido de quitação. Uma dívida só é considerada encerrada quando o usuário confirma o pagamento, e o valor real de liquidação deve ser conferido com o credor.
- A previsão D+30/60/90 começa do saldo corrente **informado manualmente** e assume que pagamentos e recebimentos não confirmados ocorrem nas datas cadastradas. Se o salário ou uma conta já estiver refletido no saldo informado, marque como recebido/pago para evitar duplicação.
- Dividendos e rendimentos podem variar, e as cotações financeiras podem estar desatualizadas. O simulador de cofrinho não é promessa de remuneração.
- Notificações do navegador só podem funcionar quando o site está aberto, com permissões concedidas e suporte do navegador. A importação de `.ics` depende do app de calendário, que controla os alarmes.
- **WhatsApp:** abre um link de mensagem pronta; o próprio usuário clica em Enviar. Não existe disparo automático nesta versão.
- Ao abrir uma nova versão no mesmo site e navegador, a aplicação tenta importar automaticamente os dados locais da versão anterior. Recomenda-se backup antes de atualizar.

---

**Kelsca Financial — Planeje hoje. Conquiste amanhã.**
