# nasa_http_requests

Fonte​ ​ oficial​ ​ do​ ​ dateset​ : ​ ​ http://ita.ee.lbl.gov/html/contrib/NASA-HTTP.html

Dados​ :
● Jul​ ​ 01​ ​ to​ ​ Jul​ ​ 31,​ ​ ASCII​ ​ format,​ ​ 20.7​ ​ MB​ ​ gzip​ ​ compressed​ , ​ ​ 205.2​ ​ MB.
● Aug​ ​ 04​ ​ to​ ​ Aug​ ​ 31,​ ​ ASCII​ ​ format,​ ​ 21.8​ ​ MB​ ​ gzip​ ​ compressed​ , ​ ​ 167.8​ ​ MB.
Sobre o dataset​ : Esses dois conjuntos de dados possuem todas as requisições HTTP para o servidor da NASA Kennedy
Space​ ​ Center​ ​ WWW​ ​ na​ ​ Flórida​ ​ para​ ​ um​ ​ período​ ​ específico.
Os​ ​ logs​ ​ estão​ ​ em​ ​ arquivos​ ​ ASCII​ ​ com​ ​ uma​ ​ linha​ ​ por​ ​ requisição​ ​ com​ ​ as​ ​ seguintes​ ​ colunas:
● Host fazendo a requisição​ . Um hostname quando possível, caso contrário o endereço de internet se o nome
não​ ​ puder​ ​ ser​ ​ identificado.
● Timestamp​ ​ no​ ​ formato​ ​ "DIA/MÊS/ANO:HH:MM:SS​ ​ TIMEZONE"
● Requisição​ ​ (entre​ ​ aspas)
● Código​ ​ do​ ​ retorno​ ​ HTTP
● Total​ ​ de​ ​ bytes​ ​ retornados

# Questões
​
Responda​ ​ as​ ​ seguintes​ ​ questões​ ​ devem​ ​ ser​ ​ desenvolvidas​ ​ em​ ​ Spark​ ​ utilizando​ ​ a ​ ​ sua​ ​ linguagem​ ​ de​ ​ preferência.
1. Número​ ​ de​ ​ hosts​ ​ únicos: 137979
2. O​ ​ total​ ​ de​ ​ erros​ ​ 404:  20871
3. Os​ ​ 5 ​ ​ URLs​ ​ que​ ​ mais​ ​ causaram​ ​ erro​ ​ 404.

+--------------------+-----+
|                host|count|
+--------------------+-----+
|hoohoo.ncsa.uiuc.edu|  251|
|piweba3y.prodigy.com|  156|
|jbiagioni.npt.nuw...|  132|
|piweba1y.prodigy.com|  114|
|www-d4.proxy.aol.com|   91|
+--------------------+-----+


4. Quantidade​ ​ de​ ​ erros​ ​ 404​ ​ por​ ​ dia.

+-----------+-----+
|        dia|count|
+-----------+-----+
|02/Jul/1995|  291|
|21/Aug/1995|  305|
|06/Aug/1995|  373|
|16/Jul/1995|  257|
|07/Aug/1995|  537|
|11/Aug/1995|  263|
|27/Jul/1995|  336|
|07/Jul/1995|  569|
|17/Jul/1995|  406|
|15/Jul/1995|  254|
|18/Jul/1995|  465|
|26/Jul/1995|  336|
|03/Aug/1995|  303|
|18/Aug/1995|  256|
|17/Aug/1995|  271|
|14/Aug/1995|  287|
|10/Jul/1995|  398|
|04/Jul/1995|  359|
|20/Aug/1995|  312|
|20/Jul/1995|  428|
+-----------+-----+

only showing top 20 rows


5. O​ ​ total​ ​ de​ ​ bytes​ ​ retornados.
+---------------+
|           Soma|
+---------------+
|6.5524319796E10|
+---------------+

-Dspark.master=local[*]
