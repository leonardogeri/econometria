

# Aula 0: Considerações Iniciais

## 1ª diferença 

$$\Delta = y_t - y_{t-1}$$

## 2ª diferença 

$$\Delta² = \Delta(\Delta y_t)=$$
$$\Delta y_t - \Delta y_{t-1}=$$
$$y_t - y_{t-1} - y_{t-1} - y_{t-2} =$$
$$y_t - 2 y_{t-1} + y_{t-2}$$

## Defasagem 

$$y_{t-1} = L y_t $$
$$L² y_t = L(L y_t) = L(y_{t-1}) = y_{t-2}$$

Aplicando a defasagem à 2ª diferença: 

$$\Delta y_t = y_t - y_{t-1}$$
$$\Delta y_t = y_t -L y_t$$
$$\Delta y_t = y_t - L y_t$$
$$\Delta y_t = (1-L) y_t$$
$$\Delta y_t = 1-L$$
$$\Delta² = (1-L)²$$
Aplicando produto notável
$= 1 -2L + L²$
$\Delta⁴ = 1-4L+6L² -4L³+l⁴$

## Séries relevantes 

### Casos extremos 

#### Termo do erro $\epsilon$ 

- $y_t = \epsilon_t \rightarrow$ ruído branco-  
- Autocorrelação dos resíduos é igual a zero 
- Termo do erro estocástico (não determinística, ou seja, aleatório)
- Obedece à distribuiçãpo $N(0,1)$, com média 0,5 (gerar diversos valores aleatórios de forma a gerar uma série que tenha essa forma)
- Precisamos encontrar um modelo que faça com que a distribuição final seja igual a essa distrivuição, de forma que não exista viés no modelo

#### Passeio aleatório (random walk) 

- $y_t = y_{t-1} + \epsilon_t$
- Existe autocorrelação 
- Passeio aleatório é definido a partir da variação do resíduo $\rightarrow$ a série se torna um ruído branco
- Série enviesada, aplicamos o operador de defasagem 

$$y_t = L y_t + \epsilon_t$$
$$\Delta y_t = \epsilon_y$$

- Logo, a variação é exatamente igual ao ruído branco (caso extremo em que os valores são perfeitamente autocorrelacionadas)


# Aula 2: Especificação do Processo Estocástico

## Definição de Komogorov

Se conhecermos as distribuições finitas dimensionais $F(x_1, x_2, ..., x_n; t_1, t_2, ..., t_n) = Pr [x(t_1), x(t_2), ... , x(t_n) \leq x_n]$, com $t_1 \in T, i=1,2,...,n$ e se elas satisfazem as condições de **simetria** e **compatibilidade**, então o processo estocástico $x(t,\omega), t \in T, \omega \in \Omega $ estará plenamente especificado.

### i) Simetria

Essa condição nos diz que, se permutarmos a ordem das distribuições de $x$, que são função do tempo, a nossa probabilidade final não muda $(F)$.

Matematicamente, temos:

$$F(x_{j1}, x_{j2}, ..., x_{jn}; t_{j1}, t_{j2},  ..., t_{jn} = $$
$$F(x_{1}, x_{2}, ..., x_{n}; t_{1}, t_{2},  ..., t_{n}$$

### ii) Compatibilidade

Para um numero grande de observações (tendendo ao infinito), as informações não acrescentam nada para entender a estrutura de probabilidade do processo estocástico. Em outras palavras, a certo ponto, diante de um determinado número de observações, jã sabemos tudo que precisamos saber sobre a distribuição. Dessa forma, podemos dispensar novas observações se as que já tivermos até então forem suficientes.  

Matematicamente, temos para $m<n$:

$$\lim_{m+1\rightarrow \infty} F(x_{1}, x_{2}, ..., x_{n}; t_{1}, t_{2},  ..., t_{n}$$
$$F(x_{1}, x_{2}, ..., x_{n}; t_{1}, t_{2},  ..., t_{n}$$

## Aplicação às Ciências Econômicas

Dentro das Ciências Econômicas, estamos diante da impossibilidade de se obter uma distribuição estatística para cada realização. Por exemplo, possuímos uma realização para o PIB de 1980, mas não um conjunto de realizações que nos forneçam a distribuição de probabilidades para o mesmo ano, o que é possível para as Ciências Exatas, por meio do laboratório. Essa dificuldade faz com que a Economia não possa se apropriar desse caso de Processo Estocástico.

Formalmente, em termos práticos, a utilização do conceito de Processo Estocástico baseado em uma especificação "estrita" é muito difícil de ser aplicado às Ciências Econômicas, pois raramente conhecemos as distribuições para processo estocástico. Alternativamente, podemos estudar as estatísticas associadas à distribuição conjunta que sejam simples de calculas e interpretar: *Primeiro e Segundo Momentos Estatísticos*. 

### Primeiro Momento: função média ou função esperança

$$\mu(t) = E[x(t)] = \int_{\infty}^{\infty} fxdx$$

### Segundo Momento: função autocovariância
Nota: A covariância mede o grau de dependência linear entre duas variáveis. 

$$\gamma (t_1, t_2) = Cov[ x (t_1_, x_2)$$
$$E[x(t_1).x(t_2)] - E[x(t_1)] . E[x(t_2)] . E[x(t_2)]$$

#### Caso específico

Para o caso específico em que falamos sobre o mesmo instante de tempo $t$, ou seja, $t_1=t_2=t$, podemos substituir os valores de $t$ na fórmula acima de $\gamma$

$$\gamma(t, t) = Cov[x(t), x(t)]$$
$$E[x(t).x(t)] - E[x(t)] . E[x(t)] . E[x(t)]$$
$$E[x(t)]²  - E[x(t)]² = Var[x(t)]$$


Ou seja, o $\gamma$ se torna a variância de $t$. 


Assim, a classe de processo estocástico não é útil para a Economia. Precisamos utilizar a classe particular dos **processos estocásticos estacionários**.  

## Processos Estocásticos Particulares

### Processo Ruído Branco 

Chamamos $y_t$ de processo ruído branco, se $E(y_t) = 0$ e $cov [y_t, ]$

Ocorre quando as ditrsibuições são independentes (covariância, ou seja, dependência linear, é igual a zero). 

### Processo Ruído Branco Gaussiano 

$$x_t ~N(\mu, \sigma_x²)$$

Se todas as médias forem iguais, a função é constante com uma distribuição com média $\mu$ e variância $\sigma²$ 

Definição: 
Copiar definição do caderno 

### Processo i.i.d.

Dizemos que $z_t$ é um processo independente e identicamente distribuído, em notação $z_t ~ i.i.d. (\mu, \sigma_z²)$, se todos os elementos de $z_t$ possuem a mesma distribuição média $\mu$ e variância $\sigma_z²$ e $cov =[$ ---> checar caderno

### Processo Random Walk 


# Aula 3: Função de Autocovariância (FACV) e Autocorrelação (FAC)

## Função de Autocovariância (em termos populacionais)

Existe dependência linear? 

$$co[x_t, x_{t \pm h}] = \gamma(t, t \pm h) = E[x_t.x_{t \pm h}] - E[x_t].E[x \pm h]$$
$$E[(x_t)- \mu_t)(x_{t \pm h}- \mu_{t \pm h})]$$

## Função de Autocorrelação

Ver caderno 

### Em termos amostrais 

Ver caderno 

## Apêndice computacional 

### Gerando um processo ruído branco gaussiano

#### Gerando uma normal 
```{r norm}
set.seed(12345)
xt <- rnorm(150, 10, 2)
plot.ts(xt)
```
