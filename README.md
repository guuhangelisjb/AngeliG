# AngeliG
O código acima é uma implementação de operações de morfologia matemática em imagens usando a biblioteca OpenCV e a linguagem Python.

Primeiro, três imagens são carregadas usando a função cv2.imread(). A imagem original é carregada na variável img, a imagem com ruído é carregada na variável img_openinge a imagem com furos é carregada na variável img_closing. Essas imagens são lidas em escala de cinza, conforme indicado pelo argumento 0passado para a função cv2.imread().

Em seguida, as dimensões da imagem original são armazenadas nas variáveis altura​​e largura.

Um kernel, representado por uma matriz de tamanho 5x5 internado com uns, é criado usando a função np.ones()do módulo NumPy. O kernel é usado como uma máscara para realizar as operações de morfologia.

O conteúdo do kernel é exibido na tela usando a função print().

As operações de morfologia são realizadas na imagem original usando as seguintes funções da biblioteca OpenCV:

cv2.erode(): Essa função realiza a operação de monitoramento na imagem, que remove os pixels da borda da imagem de acordo com o tamanho e a forma do kernel. O resultado é armazenado na variável erosion. O parâmetro iterationsdefine o número de vezes que a operação de controle é aplicada.

cv2.dilate(): Essa função realiza a operação de dilatação na imagem, que adiciona pixels à borda da imagem de acordo com o tamanho e a forma do kernel. O resultado é armazenado na variável dilation. O parâmetro iterationsdefine o número de vezes que a operação de dilatação é aplicada.

cv2.morphologyEx(): Essa função permite realizar várias operações de morfologia em uma única chamada. No código fornecido, ela é usada para calcular o gradiente morfológico da imagem original, o que resulta em uma imagem que mostra as variações de intensidade na borda dos objetos. O resultado é armazenado na variável gradient.

cv2.morphologyEx(): A função é usada novamente para aplicar a operação de abertura morfológica na imagem com ruído ( img_opening). A abertura é uma combinação de uma operação de controle seguida por uma operação de dilatação. O resultado é armazenado na variável opening.

cv2.morphologyEx(): A função é usada uma terceira vez para aplicar a operação de fechamento morfológico na imagem com furos ( img_closing). O fechamento é uma combinação de uma operação de dilatação seguida por uma operação de controle. O resultado é armazenado na variável closing.

Essas operações de morfologia são amplamente utilizadas em processamento de imagem para realizar tarefas como remoção de ruído, preenchimento de buracos, detecção de bordas e muito mais. Os resultados dessas operações podem ser usados ​​para análise posterior ou para melhorar a qualidade das imagens processadas.
