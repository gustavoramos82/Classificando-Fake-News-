# Análise de cluster das noticias verdadeiras (subject)

Neste notebook será feito a análise de cluster só que dessa vez, além do atributo título que foi feito, agora será feito com o atributo subject
Foi aplicado o algoritmo kmeans para fazer o processo de clusterização em que foi utilizado o método do cotovelo e o índice calinski-harabasz para 
verificar qual a quantidade de clusters seria o ideal.

Com o metodo do cotovelo

![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/5330e0b6-b8a0-4fb8-88ea-7146a5b45adb)

E com índice calinski-harabasz

![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/097a94b2-7f7d-46a2-ab3f-2152442d0edf)

No entanto decidu-se, para testes, começar com cincos clusters, entretanto decidu juntar os clusters 4 e 2 por serem 
muito parecidos, logo ficou em quatro cluster,que são elas:

- **Cluster 0**: Noticias com texto sobre coreia do norte, principalmente, mas outros paíse da asia, como coreia do sul, china e japão

![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/b5eafe58-685f-4b19-bd67-a55d304be694)

- **Cluster 1**: Noticias envolvendo barack obama principalmente e envolvento termos como clinton

![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/c563bdaf-9124-4045-9a79-423efe710e81)

- **Cluster 2**: Noticias envolvendo o Donal Trump

![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/cf95ea8e-b686-472d-a020-34f228519a14)

- **Cluster 3**: Noticias envolvendo principalmente a Rússia, e outros países como Turquia e Irã.

![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/8411b96d-8116-45e8-a684-c3dddd3734e0)

Assim, percebe-se que temos mais elemento do cluster 3

![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/b066450f-6b96-49ef-a377-2b8c89e5dfab)

Se compararmos em relação ao ano, vemos que o cluster 1 temos mais noticias referentes ano de 2016, enquanto os outros temos
mais noticias do ano de 2017

![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/267ef276-b343-4192-9bd4-d610c6ff9ec2)

Quanto ao tipo de conteúdo da noticia, vemos que o cluster 0 e 3 tem mais noticias referente a categoria world news, enquanto
1 e 2 tem mais noticias referentes a politcs news.

![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/74df63f0-4a73-46c8-84f9-0dafca54eeea)

