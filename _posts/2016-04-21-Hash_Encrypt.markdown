---
layout: post
title:  "La fonction de Hachage (Hash) et Chiffrement (Encryption)"
comments: true
analytics : true
category: Information
tags: hash encryption
---

### La différence entre fonction de Hachage (Hash) et Chiffrement (Encryption) ###

D'abord, il faut qu'on explique les deux brièvement.

En général, une fonction de Hachage convertit "irréversiblement" les données de tailles arbitraires aux données de tailles fixes.
De l'autre côté, il y a le Chiffrement, qui convertit les données dans une autre forme, 
tout en permettant de retrouver les données originales avec la clé de chiffrement correspondante. 

Concrètement,  il y a deux différences majeures:

- **Normalement, les tailles des données converties par une certaine fonction de Hachage ne changent jamais.** 
Mais celles obtenues par Chiffrement sont souvent (pas toujours) proportionnelles aux tailles des données originales.
Par exemple, si on utilise la fontion de Hachage encastré de Python pour convertir les deux chaînes de caractères, "Microsoft" et "Google":

{% highlight Python %}
In [22]: hash("Microsoft")
Out[22]: 467753631682903773

In [23]: hash("Google")
Out[23]: -201064995106876445
{% endhighlight %}
Les tailles de résultats sont les mêmes. Mais, si on utilise l'implémentation de RSA [^1]:
{% highlight Python %}
In [37]: (pubkey, privkey) = rsa.newkeys(512)

In [38]: rsa.encrypt("Microsoft", pubkey)
Out[38]: '\x97\xf3\xae\xf5\xea\xb5\xb9;0\x8b1xCW\xd0\xca\xd8\x07i\xf3$T\x00T\x9c\n\x88\x96Zo\x87M\x9d\x90\xe3S\xb7\xd2\xbdj><*\xadt\x15\xacz\x8e\x95\xfe|,\xdf\xfe\xd2tA<\xa8\x8fA\xee\x1e'

In [39]: rsa.encrypt("Google", pubkey)
Out[39]: "\x1b\xe4B\x82XU\xcc\xbd\x08c\x1fQ\xfbi\xd8\x19A\xf1\x18\xd1r{\xe1=\x87\xbe\xc0\xfe/\xe9\x10\x91B\x86\xc6e\xd7J!\x8e\xb5n2'v\xeb|?\x86C\xa0J~\x14\xca\x8e'\xd5G\xa3Y.\x83S"
{% endhighlight %}

- **Un algorithme de Hachage est irréversible. Au contraire, celui de Chiffrement est réversible.**
C'est-à-dire qu'il n'existe pas de façon de reconvertir les résultats générés par une fonction de hachage aux chaînes de caractères originales,
pourtant on peut déchiffrer les codes avec la clé de Chiffrement correspondante. 

{% highlight Python %}
In [40]: rsa.decrypt("\x1b\xe4B\x82XU\xcc\xbd\x08c\x1fQ\xfbi\xd8\x19A\xf1\x18\xd1r{\xe1=\x87\xbe\xc0\xfe/\xe9\x10\x91B\x86\xc6e\xd7J!\x8e\xb5n2'v\xeb|?\x86C\xa0J~\x14\xca\x8e'\xd5G\xa3Y.\x83S", privkey)
Out[40]: 'Google'

In [41]: rsa.decrypt("\x97\xf3\xae\xf5\xea\xb5\xb9;0\x8b1xCW\xd0\xca\xd8\x07i\xf3$T\x00T\x9c\n\x88\x96Zo\x87M\x9d\x90\xe3S\xb7\xd2\xbdj><*\xadt\x15\xacz\x8e\x95\xfe|,\xdf\xfe\xd2tA<\xa8\x8fA\xee\x1e", privkey)
Out[41]: 'Microsoft'
{% endhighlight %}

Pourquoi? 
Parce qu'une certaine chaîne de caractères ne peut avoir qu'un seul mapping à une autre 
chaîne de caractères, étant donné l'algorithme et la clé
(ça signifie : seul à seul).
Mais il est possible de trouver plusieurs chaînes de caractères qui peuvent convertir a un même résultat avec une certaine fountion de Hachage
(Dans cette situation, on appelle ces chaînes de caractères ont la "collision").

 
### Conception différente ###

Pour une bonne fonction de Hachage, les conditions ci-dessous doivent être satisfaites :  
- **Il est difficile de trouver quelconque collision.** 
Si on utilise une fonction de Hachage pour convertir un certain mot-de-passe, 
on peut simplement essayer une énorme quantité de chaînes de caractères afin de obtenir le même résultat,
et alors on peut passer!  
- **Elle est sensible aux petites différences.**
Si un caractère d'une chaîne avec 10000-bytes longueur est modifié, le résultat devra changer complétement. 

Et une fonction de Chiffrement fiable doit avoir la propriété de "fonction à sens unique avec trappe":  
- **Faible coût de calcul de chiffrement. Faible coût de calcul de déchiffrement, à condition de posséder la clé.**  
- **Si on n'a pas la clé, il sera extrêmement difficile de trouver l'original même si on sait l'algorithme.**  

### Référence ###

- [哈希(Hash)与加密(Encrypt)的基本原理、区别及工程应用 (en chinois)](http://www.cnblogs.com/leoo2sk/archive/2010/10/01/hash-and-encrypt.html)

### Commentaire ###

[^1]: Le chiffrement RSA est un algorithme de cryptographie asymétrique, très utilisé dans le commerce électronique, 
et plus généralement pour échanger des données confidentielles sur Internet.
