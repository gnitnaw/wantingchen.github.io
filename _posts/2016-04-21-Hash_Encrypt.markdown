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

En général, une fonction de Hachage convertit "irrévesiblement" les données avec les tailles arbitraires aux données avec les tailles fixés.
Et on peut chiffrer les données à une autre forme et aussi retrouver les données originaux avec la clé de chiffrement correspondante. 

Concrètement,  il y a deux différences majeures:

- **Normalement, les taille de données convertie par une certaine fonction de Hachage ne change jamais.** 
Mais celles obtenues par chiffrement est souvent (pas toujours) proportionnelles aux tailles de données originaux.
Par exemple, si on utilise la fontion de Hachage encastré de python pour convertir les deux chaîne de caractères, "Microsoft" et "Google":
{% highlight Python %}
In [22]: hash("Microsoft")
Out[22]: 467753631682903773

In [23]: hash("Google")
Out[23]: -201064995106876445
{% endhighlight %}
Les tailles de résultats sont la même. Mais, si on utilise l'implémentation de RSA:
{% highlight Python %}
In [37]: (pubkey, privkey) = rsa.newkeys(512)

In [38]: rsa.encrypt("Microsoft", pubkey)
Out[38]: '\x97\xf3\xae\xf5\xea\xb5\xb9;0\x8b1xCW\xd0\xca\xd8\x07i\xf3$T\x00T\x9c\n\x88\x96Zo\x87M\x9d\x90\xe3S\xb7\xd2\xbdj><*\xadt\x15\xacz\x8e\x95\xfe|,\xdf\xfe\xd2tA<\xa8\x8fA\xee\x1e'

In [39]: rsa.encrypt("Google", pubkey)
Out[39]: "\x1b\xe4B\x82XU\xcc\xbd\x08c\x1fQ\xfbi\xd8\x19A\xf1\x18\xd1r{\xe1=\x87\xbe\xc0\xfe/\xe9\x10\x91B\x86\xc6e\xd7J!\x8e\xb5n2'v\xeb|?\x86C\xa0J~\x14\xca\x8e'\xd5G\xa3Y.\x83S"
{% endhighlight %}

- **Un algorithme de Hachage est irrévisible. Néanmoins, celui de Chiffrement est révisible.**
C'est-à-dire qu'il n'existe pas de façon de retrouver les résultats générés par une fonction de hachage á les chaînes de caractères originaux,
pourtant on peut déchiffrer les codes avec la clé de chiffrement correspondante. 

{% highlight Python %}
In [40]: rsa.decrypt("\x1b\xe4B\x82XU\xcc\xbd\x08c\x1fQ\xfbi\xd8\x19A\xf1\x18\xd1r{\xe1=\x87\xbe\xc0\xfe/\xe9\x10\x91B\x86\xc6e\xd7J!\x8e\xb5n2'v\xeb|?\x86C\xa0J~\x14\xca\x8e'\xd5G\xa3Y.\x83S", privkey)
Out[40]: 'Google'

In [41]: rsa.decrypt("\x97\xf3\xae\xf5\xea\xb5\xb9;0\x8b1xCW\xd0\xca\xd8\x07i\xf3$T\x00T\x9c\n\x88\x96Zo\x87M\x9d\x90\xe3S\xb7\xd2\xbdj><*\xadt\x15\xacz\x8e\x95\xfe|,\xdf\xfe\xd2tA<\xa8\x8fA\xee\x1e", privkey)
Out[41]: 'Microsoft'
{% endhighlight %}

Pourquoi? 
Parce que une certaine chaîne de caractères peut avoir uniquement un mapping à une certaine 
chaîne de caractères avec certains algorithme et clé
(ça signifie : seul à seul).
Mais c'est possible de trouver deux ou plus chaînes de caractères qui peuvent convertir a même résultat avec une certaine fountion de Hachage
(Dans cette situation, on l'appelle ces chaînes de caractères one la "collision").

 
### Différent conception ###
Pour une bonne fonction de Hachage, il faut avoir les conditions:
- **C'est difficile de trouver quelconque collision.** 
Si on utilise une fonction de Hachage pour convertir un certain mot-de-passe, 
on peut simplement essayer une énorme quantité de chaînes de caractères afin de obtenir le même résultat,
et alors on peut passer!

- **C'est sensitive aux petites différences.**
Si un caractère d'une chaîne avec 10000-bytes longueur est modifié, le résultat devra changer complétement. 

Et une fonction de chiffrement fiable doit avoir la propriété de "fonction à sens unique avec trappe":
- **c'est facile de chiffrer facilement et aussi d'être inversé avec clé.**

- **Si on'a pas de clé, c'est extrêmement de trouver le façon de déchiffrer même si on sait l'algorithme.** 


### Référence: ###
- [哈希(Hash)与加密(Encrypt)的基本原理、区别及工程应用 (en chinois)](http://www.cnblogs.com/leoo2sk/archive/2010/10/01/hash-and-encrypt.html)
