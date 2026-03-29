# Segunda-Atividade-Pr-tica---Avaliativa---AP2-
TECNOLOGIAS MÓVEIS

Exemplo esperado:

Ramon
Magreza leve
Seu IMC: 19,54
Seu Peso: 50.0
Sua Altura: 160.0

2. Ajustar o cálculo do IMC

Fórmula:

IMC = peso / (altura * altura)

👉 Importante:

Altura geralmente vem em cm, então precisa converter para metros:
altura_m = altura / 100

3. Classificação do IMC

Use essa lógica:

IMC	Classificação
< 18.5	Magreza
18.5 - 24.9	Normal
25 - 29.9	Sobrepeso
30+	Obesidade
✅ 4. Arredondar para 2 casas decimais

Se estiver usando JavaScript:

imc.toFixed(2)

5. Alterar o layout (cores)
Trocar o tema (na imagem mudou de roxo → laranja)
Melhorar visual para parecer uma nova versão


function calcularIMC(peso, altura) {
    let alturaM = altura / 100;
    let imc = peso / (alturaM * alturaM);
    return imc.toFixed(2);
}

function classificarIMC(imc) {
    if (imc < 18.5) return "Magreza";
    else if (imc < 25) return "Normal";
    else if (imc < 30) return "Sobrepeso";
    else return "Obesidade";
}

// Exemplo
let peso = 50;
let altura = 160;

let imc = calcularIMC(peso, altura);
let classificacao = classificarIMC(imc);

console.log(`IMC: ${imc} - ${classificacao}`);
