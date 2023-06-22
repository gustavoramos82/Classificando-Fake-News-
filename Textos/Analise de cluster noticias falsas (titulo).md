# Análise de cluster das notícias Falsas (titulo)

Foi feita uma análise de cluster nas noticias falsas usando o atributo dos títulos das noticias, para isso foi usado o modelo k-means e para determinar a quantidade de clusters foi utilizado dois métodos que foi o método do cotovelo e o índice calinski-harabasz para verificar qual a quantidade de clusters seria o ideal.

Como resultado, foi esse segundo o metodo de cotovelo
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/4e109947-93be-4f36-91ac-b086dbe906bd)

E segundo o índice calinski-harabasz
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/63b1479f-e074-4201-8527-cc099fc39c24)

Observa-se que todos os dois casos tiveram cinco, então é que foi aplicado, entretanto, percebeu-se que os clusters 3 e 1 
estavam muito semlhantes então uniu os dois

Logos ficaram em quatro clusters, que são eles:

- **Cluster 0**: Noticias envolvendo black lives matter e movimento negro e racismo
  ![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/4f22b0a5-226a-411c-a5d5-aa02e229e5d5)

- **Cluster 1**: Noticias envolvendo Dolnad Trump
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/8e4f7869-30d4-4638-a357-3b2692f6768f)

- **Cluster 2**: Noticias envolvendo Obama
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/db39cb42-2054-416f-a42d-f0a7e3fffd40)

- **Cluster 3**: Noticias envolvendo a Hillari Clinton e Bill Clinton
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/ee1017c7-86ca-48a3-baf0-23333a7800fa)

Podemos ver que os clusters 1 e 2 é o que possui mais elementos se comparados com os outros dois
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/b5b7451d-72a8-4e03-88a9-cc1a85aed15d)

E que o cluster 3 a maior parte de suas noticias é do ano de 2016
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/62ab4ca0-cf01-445d-a2d4-fc086448bd03)

E que o cluster 1 a maior parte de suas noticias pertencem a categoria News disparado
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/6cb86c7e-1340-44a1-9681-d89e5fbb3393)
