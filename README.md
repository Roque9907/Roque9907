Algoritmo CalculoConsumoRestaurante
		Definir total_pagos, total_consumo, descuento, pago_cliente, consumo_cliente como Real
		Definir continuar, respuesta como Caracter
		
		total_pagos <- 0
		total_consumo <- 0
		continuar <- "S"
		
		Mientras continuar = "S" o continuar = "s"
			Escribir "Ingrese el consumo del cliente: "
			Leer consumo_cliente
			
			Si consumo_cliente > 0 Entonces
				total_consumo <- total_consumo + consumo_cliente
				
				Si consumo_cliente > 50000 Entonces
					descuento <- 0.20
				Sino
					descuento <- 0
				Fin Si
				
				pago_cliente <- consumo_cliente - (consumo_cliente * descuento)
				total_pagos <- total_pagos + pago_cliente
				
				Escribir "El cliente debe pagar: ", pago_cliente
			Sino
				Escribir "Ingrese un consumo válido."
			Fin Si
			
			Escribir "¿Desea registrar otro cliente? (S/N): "
			Leer respuesta
			
			Si respuesta = "N" o respuesta = "n" Entonces
				continuar <- "N"
			Fin Si
		Fin Mientras
		
		Escribir "Total de todos los pagos: ", total_pagos
FinAlgoritmo
