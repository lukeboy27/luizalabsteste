**INSTRUÇÕES PARA UTILIZAÇÃO DO WEBSERVICE**

OBS : No exemplo de entrada enviado não tinha a propriedade "products" no nome do array de itens, adicionei pois precisei criar uma classe como parâmetro do método que 
contemplava filtro, ordenação e agrupamento.

O endereço do endpoint é sempre o ip address da máquina, na porta "8080" seguido de "/api/main/organize", exemplo:

http://192.168.1.1:8080/api/main/organize/

Lembrando que ao subir a api pelo .jar, aparecerá o endereço do endpoint!

Abaixo seguem exemplos de entrada :

1 - Exemplo de entrada default (sem filtro, com ordenação e agrupamento padrão)

 {  
	"products" : 
		[					 
			{									
				"id":	"123",									
				"ean":	"7898100848355",									
				"title":	"Cruzador espacial Nikana - 3000m - sem garantia",									
				"brand":	"nikana",									
				"price":	820900.90,									
				"stock":	1					
			},					
			{									
				"id":	"u7042",									
				"ean":	"7898054800492",									
				"title":	"Espada de fótons Nikana Azul",									
				"brand":	"nikana",									
				"price":	2199.90,									
				"stock":	82				
			}
		]
}


2 - Exemplo de entrada com filtro.

 {  
	"products" : 
		[					 
			{									
				"id":	"123",									
				"ean":	"7898100848355",									
				"title":	"Cruzador espacial Nikana - 3000m - sem garantia",									
				"brand":	"nikana",									
				"price":	820900.90,									
				"stock":	1					
			},					
			{									
				"id":	"u7042",									
				"ean":	"7898054800492",									
				"title":	"Espada de fótons Nikana Azul",									
				"brand":	"nikana",									
				"price":	2199.90,									
				"stock":	82				
			}
		],
	"filter" : "id:123;brand:nikana"
}



3 - Exemplo de entrada com ordenação.

 {  
	"products" : 
		[					 
			{									
				"id":	"123",									
				"ean":	"7898100848355",									
				"title":	"Cruzador espacial Nikana - 3000m - sem garantia",									
				"brand":	"nikana",									
				"price":	820900.90,									
				"stock":	1					
			},					
			{									
				"id":	"u7042",									
				"ean":	"7898054800492",									
				"title":	"Espada de fótons Nikana Azul",									
				"brand":	"nikana",									
				"price":	2199.90,									
				"stock":	82				
			}
		],
	"orderBy" : "id:asc;brand:desc"
}




4 - Exemplo de entrada com agrupamento por "stock".

 {  
	"products" : 
		[					 
			{									
				"id":	"123",									
				"ean":	"7898100848355",									
				"title":	"Cruzador espacial Nikana - 3000m - sem garantia",									
				"brand":	"nikana",									
				"price":	820900.90,									
				"stock":	1					
			},					
			{									
				"id":	"u7042",									
				"ean":	"7898054800492",									
				"title":	"Espada de fótons Nikana Azul",									
				"brand":	"nikana",									
				"price":	2199.90,									
				"stock":	82				
			}
		],
	"groupBy" : "stock"
}