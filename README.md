# [**Netflix Appetency**](https://www.kaggle.com/c/netflix-appetency?utm_medium=email&utm_source=gamma&utm_campaign=community-c-spotlight-1-2022) 
(Identify consumer willing to subscribe) é uma competição promovida pela _**Prevision.io**_ na plataforma do **Kaggle**, é uma competição de aprendizado mas, com uma premiação de $300 - $200 - $100.

## **Objetivo da competição:**

Classifique os consumidores de acordo com seu apetite para assinar a Netflix.

Por razões de confidencialidade, os dados são anonimizados e aumentados.

A métrica usada é AUC

O arquivo de submissão deve ser semelhante ao arquivo sample_submission, ou seja;

```
id,target
5,0.2982
7,0.2982
9,0.2982
11,0.2982
```
### Modelos
Para este caso utilizei Ensemble Learning XgBoost e CatBoost (Decision Tree).

### Difculdades
A quantidade de fetures anonimizadas foi um problema, pois foi a primeira vez que me deparei com está situação, então tentei algumas alternativas que me auxiliassem:

* **Feature selection:** Técnica para selecionar somentes às **K** melhores features, baseado em um critério em uma _**função (f)**_, para meu caso que tomei como classificação utilizei **ANOVA**.
* **Cross Validation:** Porem não obtive melhoras.
* **Tuning:** Também utilizei pela primeira vez uma à **Otimização Bayesiana** com a lib [**bayes_opt**](https://github.com/fmfn/BayesianOptimization), foi muito bom esse estudo, porem o resultado final não melhorou o resultado obtido antes. Mas para este caso acredito que, com um melhor conhecimento da técnica e dos hiperparâmetros poderia conseguir uma melhora.

### Leaderboard

>_**Position: 98, Score: 0.78988**_
 