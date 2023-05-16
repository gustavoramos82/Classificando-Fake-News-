# Análise Inicial

Neste dataset é formada pela seguintes colunas:
-   **title**: Título do artigo
-   **text**: Texto do artigo
-   **subject**: Assunto tratado do artigo
-   **date**: Data em que foi postado

Nos artigos que não são fake news, temos notícias de dois tipos: envolvendo política e notícias internacionais.
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/5c2214b9-44e5-4a76-8b9a-47b348d9ae59)
Quanta as notícias falsas, temos mais assuntos, que são eles: notícias (acredito que seja mais geral do que os outros) e politica. Essa coluna não vai ser considerado na *modelagem*, pois os dois não tem o mesmo tipo.
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/4ab3aaac-5a82-4193-b5a1-42497aa50ead)
Após fazer um tratamento nas colunas *title*,*text* e *date*, foi feita uma análise de textos das colunas *title* e *text*.

## Análise do texto

Fazendo uma análise geral, vemos o seguinte: 

- Wordcloud do título dos artigos verdadeiros
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/6ccaf88a-b2aa-4d24-9320-b44dc6a753b3)- Wordcloud do título das fake news
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/901ea357-510c-405a-b231-aef288ebb7bc)
Comparando os títulos verifica-se que os dois falam muito sobre o Donald Trump com a diferença de que no segundo aparece sobre a hillari e tweet e no primeiro aparece notícia da Rússia

- Wordcloud dos textos dos artigos verdadeiros
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/ff3b1125-6766-4bca-ad20-566f988b5bdb)
- Wordcloud dos textos das fake news
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/a5fe343d-5228-4493-889b-1c98752b823e)
No texto das fake news aparece termos como hillary, coisa que não aparece nas notícias verdadeiras, sendo que nas notícias verdadeiras aparece o termos da coreia do norte.
