# Análise de cluster das notícias verdadeiras (titulo)

Foi feita uma análise de cluster nas noticias verdadeiras usando o atributo dos títulos das noticias, para isso foi usado o modelo
k-means e para determinar a quantidade de clusters foi utilizado dois métodos que foi o método do cotovelo e o índice calinski-harabasz
para verificar qual a quantidade de clusters seria o ideal.

Como resultado, foi esse segundo o metodo de cotovelo
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/9a65372b-cee1-42fc-961d-cbdedc5496bc)

E segundo o índice calinski-harabasz
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/4afc6cb3-93e8-40a6-a724-941eac305f21)

Foi inicialmente feito a divisão com 5 clusters, mas percebeu que os clusters 1,2 e 4 eram muito parecidos, então decidi unir os três,
ficando apenas três clusters,sendo eles:

- **Cluster 0**: Noticias relacionadas a suprema corte

![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/1720b21e-82f0-491f-92df-f163e12adc1e)

- **Cluster 1**: Noticias relacionadas principalmente ao Donald Trump, e relacionado a geopolitica como russia

![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/92bfadb0-ea25-4371-b029-1ae2590e48e0)

- **Cluster 2**: Noticias relacionas principalmente a Coreia do Norte e outros países da Ásia, como Japão e China

![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/f33255cf-4a47-4291-b5dc-9cbd244c3b7e)
