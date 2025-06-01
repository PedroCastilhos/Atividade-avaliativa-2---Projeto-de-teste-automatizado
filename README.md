# Projeto de Teste Automatizado - Qualidade de Software UniSenac

## 🎯 Descrição

Este projeto foi desenvolvido como parte da **Atividade Avaliativa 2** da unidade curricular **Qualidade de Software** do curso de Análise e Desenvolvimento de Sistemas do Centro Universitário Senac-RS.

O objetivo principal da atividade é demonstrar a aplicação prática de **testes automatizados**, contemplando dois tipos:

- ✅ **Teste funcional de sistema** (com Selenium)
- ✅ **Teste unitário** (com Pytest)

A automação foi implementada em **Python**, utilizando as bibliotecas:
- `pytest`
- `selenium`
- `webdriver-manager`

---

## 🧪 Estrutura dos testes

```bash
Atividade-avaliativa-2---Projeto-de-teste-automatizado/
├── src/
│   └── funcoes.py                  ← Função usada no teste unitário
│
├── tests/
│   ├── unit/
│   │   └── test_funcoes.py        ← Teste unitário
│   └── system/
│       └── test_login_saucedemo.py ← Teste funcional
│
├── requirements.txt
├── README.md
└── venv/ (não incluído no repositório)
```

---

## ✅ Como rodar os testes

### 1. Clone o repositório (se necessário)
```bash
git clone <url-do-repo>
cd Atividade-avaliativa-2---Projeto-de-teste-automatizado
```

### 2. Crie e ative um ambiente virtual
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Instale as dependências
```bash
pip install -r requirements.txt
```

### 4. Execute os testes
```bash
PYTHONPATH=. pytest
```

---

## 🧾 Detalhes dos testes implementados

### 🔧 Teste Unitário: `inverter_string`

Arquivo: `src/funcoes.py`

```python
def inverter_string(texto):
    return texto[::-1]
```

Arquivo de teste: `tests/unit/test_funcoes.py`

```python
from src.funcoes import inverter_string

def test_inverter_string():
    assert inverter_string("OpenAI") == "IAnepO"
```

---

### 🌐 Teste Funcional com Selenium

Site testado: [https://www.saucedemo.com/](https://www.saucedemo.com/)

Cenário: Login com usuário válido

```python
def test_login_sucesso():
    ...
    driver.get("https://www.saucedemo.com/")
    driver.find_element(...).send_keys("standard_user")
    ...
    assert "inventory" in driver.current_url
```

---

## 🖼️ Print de execução

Abaixo está um print da execução dos testes no terminal Ubuntu:

![print do pytest](prints/testes-pytest-passed.png)

---

## 👥 Integrante
- Pedro Castilhos

