# Arbitrage, Impermanent Loss

### Arbitrage

La paire fonctionne de manière autonome : son protocole calcul la parité, sans aucune relation avec les prix de marché.\
Il peut alors se produire, un décalage  : entre la parité de la paire et le prix de marché, induisant une opportunité d'arbitage.

Sur Levinswap, si la parité d'un RealTokens est très inférieure à sa valeur de marché (sur site RealT ou sur YAM), l'arbitrage consiste à acheter ce RealToken dans la pool et à le revendre à un montant plus élevé. L'arbitrageur fait ainsi, un bénéfice et fait remonter la parité de la pool.

Analysons cela, au travers d'un exemple :&#x20;

<figure><img src="../../../.gitbook/assets/image (247).png" alt=""><figcaption><p><a href="https://docs.google.com/spreadsheets/d/19Ih_NMWgKtCl9ueTH6iBlsxEUjeY7XpcbmWs1URmkQA/edit?usp=sharing">https://docs.google.com/spreadsheets/d/19Ih_NMWgKtCl9ueTH6iBlsxEUjeY7XpcbmWs1URmkQA/edit?usp=sharing</a></p></figcaption></figure>

Dans l'exemple, après une réévaluation, le RealToken est passé de 50 à 60$. Alors que la parité du pool est restée à 50$.\
Un arbitreur à acheté 2,1 RealTokens à 54,79$ l'unité, pour les revendre à 60 $ (voir plus ...). Faisant une plus value et remonter la parité de la poll à 60$.

### Impermanent Loss (IL)

l'IL est un facteur de risque important, des pools de liquidité en Defi. L'IL se produit, à l'occasion d'une variation des prix des tokens déposés sur une pool : il correspond au manque à gagner entre le dépôt de fonds sur une pool et simplement garder ses fonds (qui se valorisent, suite à la variation de prix).

Reprenons l'exemple du tableur ci-dessus.

La variation du RealToken (de 50 à 60$) a conduit le holder de la pool à faire 38,36 $ de gain (400 - 438,36). \
Si maintenant on compare ce gain, à celui qu'aurait fait le holder sans faire de dépôt : ses 4 RealTokens vaudrait 240 $ qui ajoutés aux 200 USDC ferait 440 $, soit un _Impermanent Loss_ de 1,64 $ (440 -  438,36) soit 0,37%.

Les variations des paires RealToken / USDC étant limité, le risque d'IL l'est par la même.

Le qualificatif _Impermanent_ est lié au fait que cette "perte" n'est effective que lors de la sortie de la pool. En restant dans la pool, de nouvelles variations pourraient venir corriger cette perte potentielle.