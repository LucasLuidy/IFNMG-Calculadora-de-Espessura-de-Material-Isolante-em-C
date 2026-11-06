# Calculadora de espessura de isolamento térmico em C
Programa de terminal que estima a espessura de isolamento necessária para evitar condensação na superfície externa de um meio refrigerado. O resultado é exibido em milímetros.

### Sobre a atividade
O projeto foi desenvolvido em **2023** para a disciplina de **Algoritmos e Estruturas de Dados I**, no **IFNMG Campus Salinas**. O exercício pedia duas implementações do mesmo cálculo, uma em **C** e outra em **Python**. [Ver a versão em Python](https://github.com/LucasLuidy/IFNMG-Calculadora-de-Espessura-de-Material-Isolante)

O programa estima o ponto de orvalho a partir da temperatura do ar e da umidade relativa. Depois, usa esse valor junto com a temperatura do meio refrigerado, a condutividade do isolante e os coeficientes de convecção para calcular a espessura.

### Como compilar e executar
Com o GCC instalado, rode os comandos abaixo no terminal.

```js
git clone https://github.com/LucasLuidy/IFNMG-Calculadora-de-Espessura-de-Material-Isolante-em-C.git
cd IFNMG-Calculadora-de-Espessura-de-Material-Isolante-em-C
gcc main.c -o calculadora -lm
./calculadora
```

A opção -lm vincula a biblioteca matemática usada pela função pow().

### Exemplo de uso
Digite os valores na ordem da tabela. Use ponto para separar as casas decimais.

| Dado | Unidade | Exemplo |
| --- | --- | --- |
| Temperatura de bulbo seco | °C | `25` |
| Umidade relativa do ar | % | `60` |
| Temperatura do meio refrigerado | °C | `5` |
| Condutividade térmica do isolante | W/(m·K) | `0.035` |
| Coeficiente de convecção interno | W/(m²·K) | `8` |
| Coeficiente de convecção externo | W/(m²·K) | `15` |

```js
Espessura do material isolante: 3.81 mm
```

### Limites do cálculo
O programa aplica a fórmula diretamente, sem validar as entradas. Umidade relativa de 100% ou coeficientes de convecção iguais a zero podem causar divisão por zero. Dependendo dos valores informados, a fórmula também pode produzir uma espessura negativa.

[![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)](https://github.com/LucasLuidy?tab=repositories&language=C)
