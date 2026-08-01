# Laboratório Avançado Protheus: ADVPL e TL++

Repositório dedicado ao estudo prático, desenvolvimento de customizações e integrações utilizando o ecossistema **TOTVS Protheus**.

## 🛠️ Projetos e Códigos em Destaque

### 1. Painel de Vendas Varejo em MVC (`vendas_varejo_mvc.tlpp`)
Uma rotina completa construída utilizando as melhores práticas modernas da TOTVS, unindo a nova arquitetura de linguagem e otimização de banco de dados.

- **Arquitetura MVC (Model-View-Controller):** Separação estrita de responsabilidades utilizando as classes de framework oficiais da TOTVS (`FWMBrowse`, `MPFormModel`, `FWFormView`).
- **Embedded SQL (Otimização Oracle):** Utilização das diretivas de compilação da TOTVS (`BeginSQL ... EndSQL`) para garantir o tráfego limpo de dados através do **DBAccess** para o banco de dados Oracle.
- **Regra de Negócio Aplicada:** Simulação de um painel de monitoramento de metas e fechamento diário voltado para o varejo de supermercados.

### 2. Ponto de Entrada de Alçada de Descontos (`mta410brw_desconto_varejo.tlpp`)
Implementação de customização nativa utilizando os pontos de extensão oficiais da TOTVS para o módulo de Faturamento (SIGAFAT).

- **Mecanismo de Ponto de Entrada (PE):** Uso do ponto padrão `MTA410BRW` para injeção de rotinas customizadas na interface do Pedido de Venda (`MATA410`) sem violar o núcleo do software padrão da TOTVS.
- **Domínio de Dicionário de Dados:** Manipulação avançada de metadados de tabelas do ERP, realizando a leitura direta do cabeçalho de pedidos de vendas através da tabela física `SC5` (`SC5->C5_DESCONTO` e `SC5->C5_NUM`).
- **Regra de Negócio de Varejo:** Automação de auditoria preventiva de margem de contribuição. O script avalia as taxas de desconto concedidas na operação comercial e dispara travas visuais de interface (`FWAlertWarning`) caso os limites ultrapassem as políticas de alçada da empresa, simulando um ecossistema de controle rígido de margens de supermercados.
