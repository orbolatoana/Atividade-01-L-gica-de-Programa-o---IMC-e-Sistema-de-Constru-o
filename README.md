# Atividade 01: Lógica de Programação - IMC e Sistema de Construção

### Exercício 1:
 
import kotlin.math.pow

fun main() {
    val peso = 69f
    val altura = 186f
    
    val imc = IMC(peso, altura)
    
    if (imc < 18.5) {
        println("Você está ABAIXO DO PESO! ($imc)")
    } else if (imc > 18.5 && imc < 24.9) {
        println("Você está NO PESO IDEAL. ($imc)")
    } else if (imc > 25.0 && imc < 29.9) {
        println("Você está ACIMA DO PESO! ($imc)")
    } else {
        println("Você está OBESO! ($imc)")
    }
}

fun IMC(peso: Float, altura: Float): Float {
	return peso / (altura/100).pow(2)
}

### Exercício 2: 

import kotlin.math.pow

fun main() {
    var largura = 10
    var comprimento = 10
    var area = largura * comprimento
    
    var mestre = 0
    var serventes = 0
    var engenheiros = 0
    
    var semSuite = 1
    var areaServico = 1
    var piscina = 1
    var comSuite = 1
    var banheiro = 2
    
    var subtotal = 0f
    var total = 0f
    var lucro = 0f
    
    if (area > 10){
        println("Subtottal por item:")
        
        mestre = 1
        
        serventes = (area / 10) * 2
        
        if (area >= 100){
        	engenheiros = area/100     
        }
        
        var mestreTotal = mestre * 3500
        println("Mestre: $mestreTotal")
    	var serventesTotal = serventes * 1900
        println("Serventes: $serventesTotal")
    	var engenheirosTotal = engenheiros * 11000
        println("Engenheiros: $engenheirosTotal")
    
        var areaTotal = (area/10) * 4500 
        println("Área do Terreno: $areaTotal")
    	var semSuiteTotal = semSuite * 12000
        println("Quartos sem Suíte: $semSuiteTotal")
    	var areaServicoTotal = areaServico * 15000
        println("Área de Serviço: $areaServicoTotal")
    	var piscinaTotal = piscina * 27550
        println("Piscina: $piscinaTotal")
    	var comSuiteTotal = comSuite * 17000
        println("Quartos com Suíte: $comSuiteTotal")
    	var banheiroTotal = banheiro * 5000
        println("Banheiros: $banheiroTotal")
        
        subtotal = subtotal + (mestreTotal)
        subtotal = subtotal + (serventesTotal)
        subtotal = subtotal + (engenheirosTotal)
        
        total = total + areaTotal
        total = total + semSuiteTotal
        total = total + areaServicoTotal
        total = total + piscinaTotal
        total = total + comSuiteTotal
        total = total + banheiroTotal
        total = total + subtotal
        
        println("Total sem Mão-de-Obra: \n$subtotal")
        println("Total com Mão-de-Obra: \n$total")
        
        lucro = total
        total = total * 1.25f
        lucro = total - lucro
        
        println("Custo-Final da Obra: \nR$$total")
        println("Lucro da Empresa: \nR$$lucro")
        
    } else {
        println("Erro ao contratar! A empresa só trabalha com terrenos com mais de 10m²...")
    }
}
