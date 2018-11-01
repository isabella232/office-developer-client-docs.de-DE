---
title: Grundlegendes zur Anpassungsdatei
TOCTitle: Understanding the Customization File
ms:assetid: 98fd5ec1-d5bd-cdd2-5eb5-9a1682fbed79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249686(v=office.15)
ms:contentKeyID: 48546507
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c764c543c3d8734a47927d702daca1552e497b6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879473"
---
# <a name="understanding-the-customization-file"></a>Grundlegendes zur Anpassungsdatei


**Betrifft**: Access 2013, Office 2013

Jeder Abschnittsheader in der Anpassungsdatei besteht aus eckigen Klammern (**\[**), die einen Typ und einen Parameter enthält. Die vier Abschnittstypen werden durch die Literalzeichenfolgen **connect**, **sql**, **userlist** oder **logs** angegeben. Der Parameter ist die Literalzeichenfolge, der Standardwert, ein benutzerdefinierter Bezeichner oder nichts.

Jeder Abschnitt wird daher durch einen der folgenden Abschnittsheader gekennzeichnet:

```text 
 
[ connect   default     ]
[ connect   identifier  ]
[ sql       default     ]
[ sql       identifier  ]
[ userlist  identifier  ]
[ logs                  ]
```

Die Abschnittsheader bestehen aus den folgenden Teilen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>connect</strong></p></td>
<td><p>Eine Literalzeichenfolge, durch die eine Verbindungszeichenfolge geändert wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>sql</strong></p></td>
<td><p>Eine Literalzeichenfolge, durch die eine Befehlszeichenfolge geändert wird.</p></td>
</tr>
<tr class="odd">
<td><p><strong>userlist</strong></p></td>
<td><p>Eine Literalzeichenfolge, durch die die Zugriffsrechte eines bestimmten Benutzers geändert werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>logs</strong></p></td>
<td><p>Eine Literalzeichenfolge, durch die eine Protokolldatei angegeben wird, in der Ausführungsfehler aufgezeichnet werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>default</strong></p></td>
<td><p>Eine Literalzeichenfolge, die verwendet wird, wenn kein Bezeichner angegeben ist oder gefunden wird.</p></td>
</tr>
<tr class="even">
<td><p><em>identifier</em></p></td>
<td><p>Eine Zeichenfolge, die mit einer Zeichenfolge in der <strong>connect</strong>- oder <strong>command</strong>-Zeichenfolge übereinstimmt.
</p>
<p></p>
<ul>
<li><p>Verwenden Sie diesen Abschnitt, wenn der Abschnittsheader <strong>connect</strong> enthält und die Bezeichnerzeichenfolge in der Verbindungszeichenfolge gefunden wird.</p></li>
<li><p>Verwenden Sie diesen Abschnitt, wenn der Abschnittsheader <strong>sql</strong> enthält und die Bezeichnerzeichenfolge in der Befehlszeichenfolge gefunden wird.</p></li>
<li><p>Verwenden Sie diesen Abschnitt, wenn der Abschnittsheader <strong>userlist</strong> enthält und die Bezeichnerzeichenfolge mit einem <strong>connect</strong>-Abschnittsbezeichner übereinstimmt.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


Durch **DataFactory** wird der Handler aufgerufen, dabei werden Clientparameter übergeben. Die Clientparameter werden vom Handler nach gesamten Zeichenfolgen durchsucht, die mit Bezeichnern in den entsprechenden Abschnittsheadern übereinstimmen. Wenn eine Übereinstimmung gefunden wird, wird der Inhalt dieses Abschnitts auf den Clientparameter angewendet.

Unter den folgenden Bedingungen wird ein bestimmter Abschnitt verwendet:

  - Ein Abschnitt **Verbinden** wird verwendet, wenn der Wertteil des Clients-Schlüsselworts, verbinden "**Data Source = *** Wert*", mit einem Abschnittsbezeichner **Verbinden** *.* übereinstimmt

  - Ein **sql** -Abschnitt wird verwendet, wenn die Clientbefehlszeichenfolge eine Zeichenfolge enthält, die mit einem **sql** -Abschnittsbezeichner übereinstimmt.

  - Ein **connect** - oder **sql** -Abschnitt mit einem Standardparameter wird verwendet, wenn kein entsprechender Bezeichner vorhanden ist.

  - Ein **userlist** -Abschnitt wird verwendet, wenn der **userlist** -Abschnittsbezeichner mit einem **connect** -Abschnittsbezeichner übereinstimmt. Wenn eine Übereinstimmung vorliegt, wird der Inhalt des **userlist** -Abschnitts auf die Verbindung angewendet, die dem **connect** -Abschnitt unterliegt.

  - Wenn die Zeichenfolge in einer Verbindungs- oder Befehlszeichenfolge nicht mit dem Bezeichner in einem **connect** - oder **sql** -Abschnittsheader übereinstimmt und kein **connect** - oder **sql** -Abschnittsheader mit einem Standardparameter vorhanden ist, wird die Clientzeichenfolge ohne Änderung verwendet.

  - Der **logs** -Abschnitt wird verwendet, wenn **DataFactory** ausgeführt wird.

