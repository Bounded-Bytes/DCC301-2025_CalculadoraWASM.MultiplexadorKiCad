# Repositório de Atividades Extras – AOC

### Autor: Gabriel Guilherme Figueiredo (2024005507)

Este repositório contém duas atividades extras para a disciplina de **AOC**:

1. **Calculadora WebAssembly**  
2. **Multiplexador 4x1 – KiCad e PCB**

---

## 1️⃣ Calculadora WebAssembly

- **Descrição:** Projeto de uma calculadora aritmética simples implementada em C, compilada para WebAssembly usando Emscripten, com interface HTML/JS.  
- **Ferramentas usadas:** C, Emscripten, HTML, JavaScript.  
- **Conteúdo da pasta `CalculadoraWASM`:**  
  - `index.html` → interface da calculadora  
  - `calculadora.c` → código C da calculadora  
  - `calculadora.js` e `calculadora.wasm` → arquivos gerados pelo Emscripten 

- **Como testar:**
  1. Fazer download da pasta `CalculadoraWASM`
  2. Rodar um servidor HTTP local (`python -m http.server 8000`)
  3. Abrir `http://localhost:8000` no navegador

---

## 2️⃣ Multiplexador 4x1 – KiCad

- **Descrição:** Projeto de um multiplexador 4x1, com esquemático completo e PCB pronta para fabricação.  
- **Ferramentas usadas:** KiCad.
- **Conteúdo da pasta:**
  - `multiplexador.kicad_sch` → esquemático elétrico do circuito
  - `multiplexador.kicad_pcb` → layout da placa PCB 
