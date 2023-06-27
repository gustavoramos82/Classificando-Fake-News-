# Modelagem com os algoritmos de machine learning

Agora vamos para a etapa de modelagem, inicialmente vai ser feito com os seguintes algoritmos: Regressão Logistica, Naives Bayes,
Árvore de decisão, Random Forest, Extra Tree, Grandiente Boost e Xgboost, o intuito é verificar qual o melhor modelo desses e servir
de *baseline* para os modelos de redes neurais e verificar se os mesmos tem melhor perfomace.

Comparando as métricas dos resultados, verificou-se que os três melhores que se destacaram foram
- Regressão Logistica
- Random Forest
- Extra Tree

Sendo que se for obsevado o tempo de treinamento, Extra Tree foi o que mais demorou e Regressão logistica foi o mais rápido, tendo
assim as seguintes métricas:

![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/142a0846-0d07-4611-b788-5a6d4a2629de)

|  | Regressão Logistica| Random Forest| Extra Tree|
|---|---|---|---|
|Acurácia|0.9362884160756502|0.9380614657210402|0.9421985815602837|
|Precisão|0.9396615158204562|0.9403131115459883|0.9464505035617784|
|Recall|0.9289524733268671|0.9321047526673133|0.9342870999030067|
|F1-score|0.9342763077673454|0.9361909400876767|0.9403294691885296|

Podemos ver que os três modelos tiveram uma boa perfomace, e olhando para a métricas tem pouca difrença entre elas dependendo do
que se quer poderi usar um dos três, mas usaremos o resultado do Extra Tree como *baseline*.
