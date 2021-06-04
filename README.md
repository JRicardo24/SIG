Desenvolvimento de um plugin para o QGIS, em forma de jogo, que permite ao utilizador ficar a conhecer alguns pratos típicos da Gastronomia por Distritos em Portugal.

Para obter a informação relativa a pratos típicos de cada distrito fez-se a procura e investigação da mesma distrito a distrito e inseriu-se os dados resultantes num geopackage, com 2 pratos de carne, peixe e doces por Distrito, perfazendo um total de 108 pratos. Para associar os pratos aos distritos, foi criada uma relação entre esta camada com os dados e uma camada da CAOP com os distritos de Portugal. 

Para construir o plugin foi utilizado o Plugin Builder e para apresentar as janelas de diálogo entre as diferentes fases do jogo foi usado o QTDesigner. 
Por fim, procedeu-se ao desenvolvimento das características do jogo no ficheiro gastronomia_distritos.py.

Modo de funcionamento do jogo:
- Depois de fazer o load do plugin, ao executá-lo aparece uma primeira janela onde o utilizador é questionado se pretende iniciar o jogo.
Se a resposta for positiva, são carregadas para o projeto do QGIS as duas camadas (demora alguns segundos dado que o ficheiro gpkg se encontra online) e aparece a 2ª janela de diálogo, que apresenta uma imagem e o nome do respetivo prato, escolhido aleatoriamente. O utilizador tem então de, no mapa, tentar localizar o distrito a que esse prato típico pertence. Se ao clicar no distrito este for pintado a verde, significa que acertou. Se for pintado a vermelho, significa que errou e o utilizador continua então a tentar adivinhar. Enquanto não acertar, todos os distritos escolhidos irão ficar preenchidos a vermelho. Quando finalmente acertar, as seleções erradas desaparecerão e ficará selecionado apenas o correto. Quando isto acontecer, o utilizador carrega no botão para avançar para o próximo prato e o processo repete-se 10 vezes. No final dos 10 pratos, aparece uma última caixa de diálogo a indicar que o jogo terminou. 

Desta forma, para iniciar um novo jogo bastará recarregar o plugin, sendo que o objetivo é acertar cada vez mais à 1ª tentativa e memorizar que pratos são típicos de cada distrito.
