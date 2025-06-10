# Intermediario-Oficina01-FN3 - Lista de atividades

-

1. Crie uma função que recebe dois números e retorne o maior dos dois.

function maiorNumero(num1, num2) {
    return num1 > num2 ? num1 : num2;
  }
  
  console.log(maiorNumero(15, 45)); // 45

   2. Crie uma função de calcule a potência do primeiro número elevado ao segundo número.

function potencia(base, expoente) {
    return Math.pow(base, expoente);
  }
  
  console.log('Potência:', potencia(2, 3)); // 8


  3. Calcule o fatorial de um número passado por uma função.

function fatorial(n) {
    let resultado = 1;
    for (let i = 2; i <= n; i++) {
      resultado *= i;
    }
    return resultado;
  }
  
  // Exemplo de uso:
  const numero = 5;
  console.log(`O fatorial de ${numero} é ${fatorial(numero)}`);
  // Saída: O fatorial de 5 é 120
  

  4. Calcule a área de um círculo baseada na passagem de parâmetro de seu raio.

function areaCirculo(raio) {
    return Math.PI * raio * raio;
  }
  
  // Exemplo de uso:
  const raio = 3;
  console.log(`A área do círculo de raio ${raio} é ${areaCirculo(raio)}`);
  // Saída: A área do círculo de raio 3 é 28.274333882308138



  5. Retorna apenas os números pares de um array

function numerosPares(array) {
    return array.filter(num => num % 2 === 0);
}



6. Retorna o maior número de um array

function maiorNumeroArray(array) {
    return Math.max(...array);
}

// Exemplo de uso:
const numeros = [10, 25, 7, 42, 3];
console.log(maiorNumero(numeros)); // Saída: 42


7. Gera os primeiros n números da sequência de Fibonacci

function fibonacci(n) {
    let sequencia = [0, 1];
    for (let i = 2; i < n; i++) {
        sequencia.push(sequencia[i - 1] + sequencia[i - 2]);
    }
    return sequencia;
}



8. Conta quantas vogais existem em uma string

function contarVogais(str) {
    let vogais = str.match(/[aeiouAEIOU]/g);
    return vogais ? vogais.length : 0;
}


9. Retorna se um número é par ou ímpar

function parOuImpar(num) {
    return num % 2 === 0 ? "Par" : "Ímpar";
}


10. Inverte uma string

function inverterString(str) {
    return str.split('').reverse().join('');
}


11. Calculadora básica com dois números e um operador

function calculadora(num1, num2, operador) {
    switch (operador) {
        case '+': return num1 + num2;
        case '-': return num1 - num2;
        case '*': return num1 * num2;
        case '/': return num2 !== 0 ? num1 / num2 : "Erro: divisão por zero";
        default: return "Operador inválido";
    }
}

12. Valida um CPF (formato brasileiro)

function validarCPF(cpf) {
    cpf = cpf.replace(/\D/g, '');
    if (cpf.length !== 11 || /^(\d)\1+$/.test(cpf)) return false;
    
    let calcularDigito = (parteCpf) => {
        let soma = parteCpf.reduce((acc, num, i) => acc + num * (parteCpf.length + 1 - i), 0);
        let digito = (soma * 10) % 11;
        return digito === 10 ? 0 : digito;
    };
    
    let cpfArray = cpf.split('').map(Number);
    let primeiroDigito = calcularDigito(cpfArray.slice(0, 9));
    let segundoDigito = calcularDigito(cpfArray.slice(0, 10));
    
    return primeiroDigito === cpfArray[9] && segundoDigito === cpfArray[10];
}



13. Implementa um cronômetro simples.
    
function cronometro(segundos) {
    let contador = 0;
    let intervalo = setInterval(() => {
        console.log(`${contador} segundos`);
        contador++;
        if (contador > segundos) clearInterval(intervalo);
    }, 1000);
}


  
