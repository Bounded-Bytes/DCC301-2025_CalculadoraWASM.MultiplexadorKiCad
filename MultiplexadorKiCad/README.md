# Multiplexador 4x1

Este documento descreve o projeto de um **Multiplexador 4x1** implementado com **CIs da série 74LSxx**, incluindo o **esquemático elétrico** e a **estimativa de custo de fabricação da PCB** (Placa de Circuito Impresso).

---

## 1. Descrição do Circuito

O circuito implementa a lógica booleana de um **Multiplexador 4x1**, que seleciona uma entre quatro entradas de dados (`E0`, `E1`, `E2`, `E3`) e a encaminha para uma única saída (`OUT_final`), de acordo com a combinação de dois bits seletores (`S1`, `S0`).

### **Função lógica do circuito:** $$OUT_{\text{final}} = (E_0 \cdot \overline{S_1} \cdot \overline{S_0}) + (E_1 \cdot \overline{S_1} \cdot S_0) + (E_2 \cdot S_1 \cdot \overline{S_0}) + (E_3 \cdot S_1 \cdot S_0)$$

diagrama esquemático do multiplexador
---

## 2. Lista de Componentes

| Componente | Quantidade | Custo Unitário Médio (R$) | Custo Total (R$) | Observações |
|:--|:--:|:--:|:--:|:--:|
| CI 74LS11 (Porta AND – 3 entradas) | 2 | 3,00 | 6,00 | 4 portas AND necessárias (3 do U1, 1 do U2) |
| CI 74LS04 (Inversor NOT) | 1 | 2,50 | 2,50 | Geração de $\overline{S_1}$ e $\overline{S_0}$ |
| CI 74LS32 (Porta OR – 2 entradas) | 1 | 2,50 | 2,50 | Três portas em cascata para OR de 4 entradas |
| Chave Nidec CAS-120A1 (SPDT Deslizante) | 6 | 2,00 | 12,00 | Chaves seletoras SPDT 3 pinos |
| Conector Pin Header (Conn_01x01) | 3 | 0,50 | 1,50 | Para VCC, GND e saída de dados ($OUT_{\text{final}}$).
| Resistor 330 Ω (1/4 W) | 1 | 0,50 | 0,50 | Limita corrente do LED |
| Mini LED (3 mm) | 1 | 1,00 | 1,00 | Indica visualmente a saída HIGH |
| **TOTAL** |  |  | **R$ 26,00** |

---

## 3. Estimativa de Custo de Produção da PCB

A tabela abaixo mostra o custo médio de **componentes** e **fabricação** em protótipo de placa dupla face (aprox. 5 × 5 cm):

| Item | Quantidade | Custo Unitário (R$) | 
|:--|:--:|:--:|
| Custo dos componentes | 1 | 26,00 |
| Fabricação da placa (PCB – 5×5 cm, dupla face) | 1 | 18,00 – 36,00 |
| **Custo total estimado por placa** |  | **R$ 44,00 – 62,00** | 

**Detalhe:**  
O custo de fabricação (R$ 18 – 36 por unidade) foi obtido a partir da divisão do custo total de um lote de 5 placas (≈ R$ 90 – 180) em serviços de prototipagem de PCBs.

---

## 4. Arquivos do Projeto

- `multiplexador.kicad_sch` → esquemático elétrico do circuito
- `multiplexador.kicad_pcb` → layout da placa PCB 


