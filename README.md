# Laboratório Avançado Protheus: ADVPL e TL++

Repositório dedicado ao estudo prático, desenvolvimento de customizações e integrações utilizando o ecossistema **TOTVS Protheus**.

## 🛠️ Projetos e Códigos em Destaque

### 1. Painel de Vendas Varejo em MVC (`vendas_varejo_mvc.tlpp`)
Uma rotina completa construída utilizando as melhores práticas modernas da TOTVS, unindo a nova arquitetura de linguagem e otimização de banco de dados.

- **Arquitetura MVC (Model-View-Controller):** Separação estrita de responsabilidades utilizando as classes de framework oficiais da TOTVS (`FWMBrowse`, `MPFormModel`, `FWFormView`).
- **Embedded SQL (Otimização Oracle):** Utilização das diretivas de compilação da TOTVS (`BeginSQL ... EndSQL`) para garantir o tráfego limpo de dados através do **DBAccess** para o banco de dados Oracle.
- **Regra de Negócio Aplicada:** Simulação de um painel de monitoramento de metas e fechamento diário voltado para o varejo de supermercados.
