# Sistema de Reconhecimento Facial 


## Visão Geral do Projeto

Este projeto demonstra um pipeline completo para treinar e testar um modelo de detecção de faces com **YOLOv5** no **Google Colab**.

Foi utilizado o mesmo codigo do projeto [cezarcorrea-Deteccao-Gato-Cachorro](https://github.com/cezarcorrea/cezarcorrea-Deteccao-Gato-Cachorro), com apenas algumas modificaçãos nas pastas principais e nos arquivos de treinamento, por conter mais de um objeto a ser detectado, foi necessario criar um dataset com mais de 60 imagens de treinamento sendo necessario executar a 200 epochs ou superior.

## Características Principais

- **Detecção de Objetos:** Implementa a detecção de objetos para as classes cat e dog usando a arquitetura de última geração YOLOv5.

- **Treinamento Otimizado:** O modelo é treinado com transfer learning a partir dos pesos pré-treinados yolov5s.pt, o que permite um aprendizado rápido e eficiente com um conjunto de dados personalizado.

- **Ambiente do Google Colab:** O projeto foi desenvolvido para ser executado de forma fluida no Google Colab, desde a configuração inicial até a detecção final.

- **Automação de Pipeline:** O script automatiza a instalação das dependências, o treinamento do modelo e a detecção em uma imagem de teste, simplificando o processo para o usuário.

- **Gerenciamento de Pastas Dinâmico:** O código identifica automaticamente a pasta de treinamento mais recente (exp, exp2, etc.) para garantir que a detecção use o modelo mais atualizado.

## Tecnologias Utilizadas

- **YOLOv5:** Uma das redes neurais de detecção de objetos mais rápidas e precisas.

- **Python:** Linguagem principal para os scripts de treinamento e detecção.

- **PyTorch:** Biblioteca de machine learning subjacente ao **YOLOv5**.

- **Google Colab:** Plataforma de notebook baseada em nuvem com acesso gratuito a GPUs.

- **Git:** Utilizado para clonar o repositório da **Ultralytics**.

## Como Executar o Projeto

Para treinar e testar este modelo, siga os passos abaixo em um notebook do Google Colab:

1- Faça o upload do seu conjunto de dados de treino e validação (images e labels) para o seu Google Drive, seguindo a estrutura de pastas especificada no código.

2- Abra o notebook e execute todas as células na ordem.

3- O script irá clonar o repositório YOLOv5, instalar as dependências, treinar o modelo, e por fim, realizar a detecção em sua imagem de teste.

O resultado da detecção será salvo em uma pasta de resultados, mostrando as caixas delimitadoras e a confiança do modelo para cada detecção.

## Estrutura de Pastas

Para que o projeto funcione corretamente, a base de dados de imagens deve seguir a seguinte estrutura no seu **Google Drive:**

```
/meu_projeto_rostos
├── /data
│   ├── /images
│   │   ├── /train
│   │   │   └── img1.jpg
│   │   │   └── img2.jpg
│   │   └── /val
│   │       └── img_val1.jpg
│   └── /labels
│       ├── /train
│       │   └── img1.txt
│       │   └── img2.txt
│       └── /val
│           └── img_val1.txt
├── /runs
│   └── /train
│       ├── /exp
│       ├── /exp2
│       └── ...
├── /teste
│   └── image.jpg
├── data.yaml
└── yolov5/
```

## Resultado da detecção na imagem de teste.


![Image](https://github.com/user-attachments/assets/02349424-c6f3-4c29-9585-457858d72d69)

### 📜 Licença
Este projeto está licenciado sob a Licença MIT.

### 📫 Contato

Fique à vontade para visitar meu perfil no GitHub: [@cezarcorrea](https://github.com/cezarcorrea)

---
