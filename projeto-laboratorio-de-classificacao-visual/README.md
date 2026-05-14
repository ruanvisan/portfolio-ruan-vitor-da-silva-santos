# 🧠 Laboratório de Classificação Visual

Projeto de classificação de imagens utilizando **TensorFlow.js** e **Teachable Machine**, focado na identificação de categorias visuais através de inteligência artificial diretamente no navegador.

---

## 📌 Sobre o Projeto

O **Laboratório de Classificação Visual** é um modelo de Machine Learning treinado para reconhecer imagens e classificá-las em duas categorias:

- **Operacional**
- **Liderança**

O projeto foi exportado através do **Google Teachable Machine**, utilizando uma arquitetura baseada em redes neurais convolucionais (CNN) com TensorFlow.js.

O objetivo é permitir testes rápidos de reconhecimento visual em aplicações web sem necessidade de processamento em servidor.

---

## 🚀 Tecnologias Utilizadas

- JavaScript
- TensorFlow.js
- Teachable Machine
- HTML5
- CSS3

---

## 🧩 Estrutura do Projeto

```bash
.
├── README.md
├── metadata.json
├── model.json
├── weights.bin
```

### Arquivos principais

| Arquivo | Descrição |
|---|---|
| `model.json` | Estrutura do modelo treinado |
| `weights.bin` | Pesos da rede neural |
| `metadata.json` | Informações do modelo e classes |
| `README.md` | Documentação do projeto |

---

## 🏷️ Classes do Modelo

O modelo foi treinado com as seguintes categorias:

| Classe | Descrição |
|---|---|
(/img.png)
| Operacional | Imagens relacionadas ao ambiente operacional |
| Liderança | Imagens relacionadas a liderança e gestão |

---

## ⚙️ Informações Técnicas do Modelo

| Configuração | Valor |
|---|---|
| Framework | TensorFlow.js |
| Exportação | Teachable Machine |
| Versão TFJS | 1.7.4 |
| Versão TM | 2.4.14 |
| Tamanho da imagem | 224x224 |
| Quantidade de classes | 2 |

---

## 📷 Como Utilizar

### 1. Clone o repositório

```bash
git clone https://github.com/ruanvisan/portfolio-ruan-vitor-da-silva-santos/tree/main/projeto-laboratorio-de-classificacao-visual.git
```

### 2. Abra o projeto

Você pode utilizar:

- VS Code
- Live Server
- Qualquer servidor local

---

## 🖥️ Exemplo de Implementação

```html
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@latest"></script>
<script src="https://cdn.jsdelivr.net/npm/@teachablemachine/image@latest"></script>

<script>
const URL = "./";

let model;

async function carregarModelo() {
    const modelURL = URL + "model.json";
    const metadataURL = URL + "metadata.json";

    model = await tmImage.load(modelURL, metadataURL);
    console.log("Modelo carregado!");
}

async function preverImagem(imagem) {
    const previsoes = await model.predict(imagem);

    previsoes.forEach(previsao => {
        console.log(
            `${previsao.className}: ${previsao.probability.toFixed(2)}`
        );
    });
}

carregarModelo();
</script>
```

---

## 🧪 Funcionamento

1. O usuário envia ou captura uma imagem.
2. A imagem é redimensionada para `224x224`.
3. O TensorFlow.js processa a imagem.
4. O modelo retorna a probabilidade de cada classe.
5. A classe com maior confiança é exibida.

---

## 📊 Arquitetura Utilizada

O modelo exportado utiliza uma arquitetura convolucional otimizada para aplicações web, baseada em:

- CNN (Convolutional Neural Network)
- MobileNet
- TensorFlow.js Layers API

Essa abordagem permite:

- Execução diretamente no navegador
- Baixo consumo de recursos
- Inferência rápida
- Facilidade de integração em aplicações web

---

## 🌐 Possíveis Aplicações

- Sistemas de triagem visual
- Classificação automatizada
- Dashboards inteligentes
- Ferramentas educacionais
- Sistemas internos corporativos
- Reconhecimento visual em tempo real

---

## 📦 Requisitos

- Navegador moderno
- JavaScript habilitado
- Servidor local (recomendado)

---

## 🔮 Melhorias Futuras

- Interface gráfica completa
- Upload de imagem via drag and drop
- Captura por webcam
- Mais categorias de classificação
- Dashboard de métricas
- Treinamento contínuo do modelo

---

## 👨‍💻 Autor

Projeto desenvolvido para estudos e experimentação com classificação visual utilizando inteligência artificial no navegador.

---

## 📄 Licença

Este projeto está disponível para fins educacionais e de aprendizado.

