#Seminaire Crypto

##Introduction

Les 4 buts de la crypthographie

- Confidentialité:

    Mécanisme pour transmettre des données de telle sorte que seule le destinataire puisse le lire

- Intégrité:

    Mécaninisme pour s'assurer que les données recues n'ont pas été modifiées durant la transaction

- Authentification:

    Mécanisme pour permettre d'indetifier les personnes, les entités et de cetifié cette identité

- Non répudiation:

    Mécanisme permettant d'entrigstrer un acte ouu un engagement d'une personne ou d'une entité de telle sorte que celle-ci ne puisse nier avoir accomplie l'acte ou l'engagement
    
    
###Qu'est ce qu'un crypthosytème?
Le chiffrement d'un message consiste à le coder (ou plutot à le chiffer) pouir le rendre incompréhensible pour quiconque n'est pasdoté d'une clé de déchiffrement (Kd)

L'activité de crypthographie est très ancienne puisqu'elle remonte à l'antiquité (6em siècle avant JC)

Dans un cryptosystème, on distingue:
    
- L'espace des messages clairs M dans une alphabet A
- L'espace des lessages chiffres C dans un alphabet B (en général A=B)
- L'espace de clés K
- Un ensemble E de transformation de chiffrement (chaque transformation étant indexée par une clée) tel que EK: m appartementant a M -> c appartient C
- Un ensemble D de transformation de déchiffrement et évidement
    - DK: c appartient C => m appartenant M
    - DKd (EKe(m)) = m || Crypto symétrique d = e
        

Kerkoffs a enoncé à la fun du XIX siècle que la sécurité d'un cryothosytème ne doit pas reposer sur la divulgation des fonctions de chiffrement et déchiffrerement  utilisées mais sur la non divulgation des clées pour les paramétrer.

###Quelques rappels historiques (recent)

- Jusqu'au milieur des années 70, les cryposystèmes étaient symétrique, c'est à dire que c'est la meme clé qui permmetent de configurer les fonctions de chiffrement et de déchiffrement. Se pose alors le problème crucial de l'échange de clée entre ess interlocuteurs, imposible à résoudre dans le cas d'un système développer à grande échelle.

- en 1976, Deffie et Hellman introduise le concept de cryptographie à clé publique. C'est à dire que pour écrire à une personne on utilse sa clé pinlic pour chiffrer le message et seul sa clé privée lui permettra de la déchiffré (53 biclé)

- En 1978, premiere implémentation d'un cryptosystème asymétrique introduisant par Rivest Shamir et Adleman: RSA. Ce système est l'uns de seyles à avoir ressister a la cryptanalyse. La cryptographie asymétrique donnerra naissance à d'autre concepts comme celui de la signature électronique (où l'authenticité l'emmeteur doit etre assuré pour garantir la non répudiation)

##Les grands types de menace

- Menaces passives
    - On ne fait qu'écouter le message
        - menace la confidentialité puisqu'une information sensible pourra parvenir à une autre personne que celle légitime.
        
- Menaces actives
    - On cherche à modifier le contenu du message
    - Menace l'intégrité

####Quelques exemples:

- usurpation de l'identité (de l'emetteur ou du recepteur)
- Alteration / modification du message
- Destruction du message ou retardemment de transmission
- Répétion du message (jusqu'a l'engorgement)
- Répudiation du message (l'emetteur du message nie avoir envoyé le message)

###La cryptoanalyse
La cryptanalyse st l'étude de la s"curité des procédés de chiffrement utilisé en cryptographie.

On distingue 4 niveauxd'attaque possible

- Texte chiffré connu: Seul C est connu de l'attaquant
- Texte clair connu: l'attaquant connait C et M correspondant
- Texte clair choisi: Pour tout M ont peut obtenir C
- Texte chiffré choisi: pour tout C on peut obtenir M

####Principe de Modélisation de l'adversaire:
On doit modéliser un attanquant

- Le plus intéligent possible; Il peut fair toutes les opérations qu'il souhaite
- Qui dispose d'un temps limité
    - Il existe un temps limité partir duquel l'algorithme est considérer comme fiable
    - Sinon l'adversaire peut toujours énumerer toutes les clés

- Les principaux algorythmes d'attaque

- Attaque brutale
    - Enumérer toutes les valeurs possibles de clé:
    pour information 64bits = 2⁶⁴ = 1.844 * 10¹⁹
    Au rythme d'1 milliard de clé par seconde il faudrait 1 an sur 584 machines machines pour énumérerr toutes les clées
    
- Attaque par séquences séquencielle connu
deviner la clé si une partie du message est cibby (exemple les en-tetes de mail ont un pattern connu)

- Attaque par séquence forcées:
Qui consiste à faire chiffrer par la victile un bloc dont l'attaquant connait le contenu puis on applique la méthode précédente

- Attaque par analyse différentielle
Utiliser une faible différence entre plusieurs messages (exemple des logso pour deviner la clé)

####Chiffrement par substitution
Ce chiffrement constite à remplacer dans un meessage une ou plusiers entité (généralement des lettres) par un ou plusiers autre entités

On distingue plusierurs types de cryptosystees ar substitution.

- La substitution monoalphabétique: consiste à remplacer chaque lettre du message par une autre lettre de l'alphabet.
- Substitution polyalphabétique: qui consiste à réutiliser une suite de chiffres monoalphabétique périodiquement
- Subsitution homophonique consiste à faire correspondre à chaque lettre du message en clair un ensemble possible d'autre caractères.

Subsitution de polygrammes:
Consiste à substituer un groupe de caractère (polygrammes) dans le message oar un autre groupe de caractères

