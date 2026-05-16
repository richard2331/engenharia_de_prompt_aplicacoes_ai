# Projeto Módulo 3 – Low Code/No Code/Vibecode

## 📌 Desafio Escolhido

O grupo desenvolveu um **sistema de gestão completo para lojistas**, resolvendo um problema real enfrentado por donos de pequenas lojas: a fragmentação do gerenciamento em planilhas separadas e ferramentas desconectadas.

O protótipo centraliza em uma única aplicação:
- Cadastro e controle de estoque com alertas automáticos de reposição
- Gerenciamento de funcionários com horários de entrada, saída e almoço
- Ponto eletrônico diário com cálculo automático de horas trabalhadas
- Contas a pagar e a receber com alertas de vencimento
- Tabela de preços com cálculo automático de margem de lucro
- Dashboard unificado com KPIs e alertas críticos em tempo real

---

## 🖥️ Protótipo

* Prints das telas na pasta `/docs`
* O protótipo funciona como um arquivo HTML único que roda diretamente no navegador, sem instalação ou internet

**Como usar:**
1. Abrir o arquivo `gestaoloja.html` no navegador
2. Clicar em **"Criar conta"** e preencher nome da loja, nome, email e senha
3. Fazer login e começar a usar o sistema completo

Todos os dados são salvos automaticamente no próprio navegador (`localStorage`), sem necessidade de servidor ou banco de dados externo.

---

## ⚙️ Plataforma Utilizada

* **Nome da plataforma:** HTML + CSS + JavaScript puro (abordagem Vibecode)

* **Justificativa da escolha:** A abordagem vibecode foi selecionada por permitir construir um protótipo funcional completo em uma única sessão, sem dependência de plataformas externas como Bubble ou Make. Como o desafio envolvia múltiplos módulos integrados (estoque, RH, financeiro), plataformas no-code teriam dificuldade em conectar todos esses fluxos sem planos pagos. O HTML puro garantiu liberdade total de personalização, funcionamento offline e zero custo — características ideais para validar o conceito com usuários reais antes de investir em infraestrutura.

---

## ✅ Vantagens Identificadas

Liste pelo menos 3 vantagens percebidas no uso da abordagem low code/no code/vibecode:

1. **Prototipagem rápida** — sistema completo funcional desenvolvido em uma única sessão, sem configuração de servidores ou banco de dados
2. **Zero dependência externa** — o arquivo roda offline, sem conta em plataforma, sem custo e sem risco de descontinuação do serviço
3. **Personalização total** — cores, fluxos e regras de negócio completamente controlados, sem as restrições de blocos visuais de plataformas no-code
4. **Dados privados** — as informações ficam no próprio dispositivo do lojista, sem passar por servidores de terceiros
5. **Integração nativa entre módulos** — estoque, financeiro, ponto e funcionários compartilham os mesmos dados em tempo real, sem conectores ou automações extras

---

## ⚠️ Limitações Encontradas

Liste pelo menos 3 limitações percebidas:

1. **Customização limitada para escala** — sem banco de dados real, os dados não sincronizam entre dispositivos diferentes
2. **Dependência do navegador** — limpar o cache apaga todos os dados, o que seria inaceitável em produção
3. **Risco de lock-in tecnológico** — ao evitar plataformas no-code, o grupo assumiu total responsabilidade pelo código; qualquer evolução depende de desenvolvimento manual
4. **Sem exportação de relatórios** — não é possível gerar PDF ou planilha para o contador
5. **Sem acesso simultâneo** — funcionários não conseguem registrar ponto de dispositivos diferentes

---

## 📚 Reflexão Crítica

O grupo identificou que as limitações mais críticas — sincronização entre dispositivos e ausência de backup — são exatamente os problemas que plataformas como Bubble ou Supabase resolveriam nativamente, mas a custo de dependência e menor controle sobre os dados.

A solução criativa adotada foi usar o `localStorage` com dados isolados por usuário, simulando o comportamento de um banco de dados multi-tenant sem infraestrutura real. Isso permitiu que múltiplas contas de loja coexistissem no mesmo arquivo sem interferência entre si.

A experiência confirmou o diagnóstico da Unidade III: vibecode brilha na validação rápida de ideias, mas encontra seu teto natural quando o produto precisa de persistência em nuvem e colaboração em tempo real. O caminho ideal seria usar este protótipo para validar o interesse dos lojistas e, confirmada a demanda, migrar para uma stack com banco de dados real.

---

## 👥 Colaboração

- Richard de Souza Dias
- Matheo Augustus Rocha Bagatini
- João Miguel Monteiro Lima
- João Pedro Mota Borges Baía

---

## 📝 Registro da Aula

| Campo | Informação |
|---|---|
| **Data** | 11/05/2026 |
| **Atividade** | Discussão crítica + mini-projeto de aplicação |
| **Local** | Laboratório de informática / Quadro branco |
| **Professor(a)** | Kadidja Valéria |

---

## 🚀 Próximos Passos

* Adicionar exportação de dados em JSON para backup manual entre dispositivos
* Implementar geração de relatório PDF de ponto mensal por funcionário
* Migrar o armazenamento de `localStorage` para Supabase, mantendo a mesma interface visual
* Adicionar módulo de metas de vendas com acompanhamento diário
* Criar versão mobile-first para que funcionários registrem o ponto pelo celular
* Evoluir para o Projeto Final da Unidade 3 com autenticação real e dados em nuvem
