# Digital Innovation One

Código criado para utilização junto a plataforma da Digital Innovation One

<p align="center"><img src="./Logo.png" width="500"></p>

## Darknet Project

Este projeto é baseado no Darknet, uma estrutura de código aberto escrita em C e CUDA para treinamento e inferência de redes neurais convolucionais, com foco em detecção de objetos usando o algoritmo YOLO (You Only Look Once).

## Requisitos

- Linux
- CUDA
- OpenCV

Certifique-se de ter instalado todas as dependências necessárias antes de prosseguir.

## Configuração

1. Clone o repositório Darknet:

   ```bash
   git clone https://github.com/AlexeyAB/darknet.git

Compile o Darknet:

bash
Copy code
cd darknet
make
Certifique-se de ajustar as configurações do Makefile, como a GPU e o OpenCV, conforme necessário.

Faça o download dos pesos pré-treinados do modelo YOLOv3:

bash
Copy code
wget https://pjreddie.com/media/files/yolov3.weights
Treine a rede neural:

bash
Copy code
./darknet detector train obj.data yolov3.cfg yolov3.weights -dont_show
Certifique-se de ter preparado corretamente os dados de treinamento, incluindo o arquivo obj.data e a configuração da rede yolov3.cfg.

Execute a detecção de objetos:

bash
Copy code
./darknet detect obj.data yolov3.cfg yolov3.weights data/person.jpg -dont-show
Isso executará a detecção de objetos na imagem person.jpg usando o modelo treinado.

Referências
Darknet repository: https://github.com/AlexeyAB/darknet
YOLO: Real-Time Object Detection: https://pjreddie.com/darknet/yolo/
Licença



