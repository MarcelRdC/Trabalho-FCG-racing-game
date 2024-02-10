# Trabalho-FCG-racing-game

## Participação
	Este repositório conta com somente minhas alterações sobre o código escrito originalmente pelo professor Eduardo Gastal.
## Ferramentas de IA utilizadas
	Há um trecho de código escrito por ChatGPT que implementa uma Curva de Bézier. Essa ferramenta foi útil pois o código gerado está compreensível e funcional.

## Conceitos de Computação Gráfica

# Malhas poligonais complexas
	A aplicação conta com 3 carros em formato .obj obtido no site turbosquid.com.
# Transformações geométricas controladas pelo usuário
	As transformações geométricas controladas pelo usuário são a translação e a rotação do carro. Não houve problemas de implementação.

# Câmera livre e câmera look-at
	A câmera free é ligada ao movimento do carro, e a transição entre câmeras free e look-at é problemática porque qualquer mudança no ângulo da câmera afeta a movimentação esperada do carro.

# Instâncias de objetos
	As paredes do circuito foram feitas com várias instanciações de um único objeto, que foram devidamente posicionadas de acordo com geometria e trigonometria.

# <s>Três tipos de testes de intersecção</s>
	Não foram implementados.

# Modelos de Iluminação Difusa e Blinn-Phong
	Os modelos de iluminação foram copiados do código feito para o Laboratório 4 do professor Eduardo Gastal.

# <s>Modelos de Interpolação de Phong e Gouraud</s>
	Não foram implementados.

# Mapeamento de texturas em todos os objetos
	A aplicação consta com 4 diferentes texturas, uma para cada objeto que compõe a aplicação. A adição de chamadas de "glUniform1i(glGetUniformLocation(g_GpuProgramID, "TextureImageN"), N);" na função LoadShadersFromFiles() do arquivo main.cpp resolveu o problema de texturas não carregando.

# Movimentação com curva Bézier cúbica
	O algoritmo utilizado, como já mencionado, foi gerado por ChatGPT. Um problema observado foi a movimentação dos carros que andam na Curva de Bézier se dando, por vezes, no sentido oposto. Esse problema foi causado pela aplicação da variável "delta_t" ao valor cumulativo "t" usado como parâmetro na Curva de Bézier, quando ao invés disso, deveria ser aplicada somente ao valor a ser incrementado a "t".

# Animações baseadas no tempo ($\Delta t$) 
	A movimentação do carro do jogador, juntamente com a movimentação dos demais carros na Curva de Bézier, possui um fator chamado delta_t que hegemoniza a velocidade dos carros em diferentes hardwares.

https://cdn.discordapp.com/attachments/1115109755711664260/1205700953332912238/image.png?ex=65d95384&is=65c6de84&hm=bdd0401096749428dc0f2058e7b73b4ea6f1d19d76253682e0c1e22bec9f503f&
https://cdn.discordapp.com/attachments/1115109755711664260/1205701094118785125/image.png?ex=65d953a5&is=65c6dea5&hm=63d512ddbedc700383bdc8c4f6a34d2f0736f0b69ab15b217ec52daf08e10af3&

## Manual
	[W] Aumenta a velocidade do carro para a frente.
	[S] Diminui a velocidade do carro para frente.
	[A] Rotaciona o carro para a esquerda (se andando para a frente).
	[D] Rotaciona o carro para a direita (se andando para a frente).
	[F] Retorna à posição inicial.
	[C] Muda a câmera de semi-free para look-at.
	<s>[SPACE] Pula.</s>