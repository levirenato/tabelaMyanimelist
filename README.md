# Tabela de animes populares no site MyAnmeList
Tabela gerada a partir de webScrapping, com informações de animes populares no site

# Introdução
Para fins de aprendizado resolvi analisar uma tabela de animes no site MyAnimeList, no entanto a tabela retornada tinha alguns problemas.
![image](https://github.com/levirenato/tabelaMyanimelist/assets/84652664/dd55a950-a61f-43ed-8a3f-10e658d37a20)

O primeiro é que ela é muito limitada, não tem informações de categoria do anime e faixa étaria. O segundo problema é que as informações que são exibidas além do titulo são textos separados por quebra de linha tudo dentro da mesma tag, ou seja informações como ano de lançamento, quantidade de membros e tipo de anime(Tv, filme, ova, ...) estão dentor do titulo. Como na imagem abaixo:

![image](https://github.com/levirenato/tabelaMyanimelist/assets/84652664/42a0295b-c155-4273-8314-a142feb81d1e)

*tabela retornada por padrão usando o pandas*

Com isso decidi que iria criar um notebook que me retorna exatamente as informações que eu preciso.

### Bibliotecas usadas:
* BeautifulSoup;
* Pandas;
* Regex;

# Solução
Usei o regex para separar cada item a partir do padrão

![image](https://github.com/levirenato/tabelaMyanimelist/assets/84652664/c4dff45e-1980-43e3-90de-11f4b4b7336f)

Mas ainda falta as informações que só temos ao acessar a pagina do anime selecionado, com isso decidi fazer um looping que entra em cada link, guarda as informções requisitadas numa lista para depois adicionar isto ao datafreame.

*Resultando na tabela final:*

![image](https://github.com/levirenato/tabelaMyanimelist/assets/84652664/52c20599-685c-4823-8831-6e807d7b84a6)
