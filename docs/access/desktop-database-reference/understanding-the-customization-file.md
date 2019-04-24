---
title: Grundlegendes zur Anpassungsdatei
TOCTitle: Understanding the Customization File
ms:assetid: 98fd5ec1-d5bd-cdd2-5eb5-9a1682fbed79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249686(v=office.15)
ms:contentKeyID: 48546507
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b977fc4273068ac52efe8960761a9e28a6234e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314070"
---
# <a name="understanding-the-customization-file"></a>Grundlegendes zur Anpassungsdatei


**Gilt für**: Access 2013, Office 2013

Jeder Abschnittskopf in der Anpassungsdatei besteht aus eckigen Klammern**\[**() mit einem Typ und Parameter. Die vier Abschnittstypen werden durch die Literalzeichenfolgen **connect**, **sql**, **userlist** oder **logs** angegeben. Der Parameter ist die Literalzeichenfolge, der Standardwert, ein benutzerdefinierter Bezeichner oder nichts.

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
<th><p>Teil</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>verbinden</strong></p></td>
<td><p>Eine Literalzeichenfolge, durch die eine Verbindungszeichenfolge geändert wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>SQL</strong></p></td>
<td><p>Eine Literalzeichenfolge, durch die eine Befehlszeichenfolge geändert wird.</p></td>
</tr>
<tr class="odd">
<td><p><strong>UserList</strong></p></td>
<td><p>Eine Literalzeichenfolge, durch die die Zugriffsrechte eines bestimmten Benutzers geändert werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>Protokolle</strong></p></td>
<td><p>Eine Literalzeichenfolge, durch die eine Protokolldatei angegeben wird, in der Ausführungsfehler aufgezeichnet werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>default</strong></p></td>
<td><p>Eine Literalzeichenfolge, die verwendet wird, wenn kein Bezeichner angegeben ist oder gefunden wird.</p></td>
</tr>
<tr class="even">
<td><p><em>Bezeichner</em></p></td>
<td><p>Eine Zeichenfolge, die mit einer Zeichenfolge in der <strong>connect</strong>- oder <strong>command</strong>-Zeichenfolge übereinstimmt.</p>
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

  - Ein **Connect** -Abschnitt wird verwendet, wenn der Wert Teil des Schlüsselwortes Client Connect String, "**Data Source = * * * * value*", **mit einem Connect** -Abschnitts Bezeichner übereinstimmt *.*

  - Ein **sql** -Abschnitt wird verwendet, wenn die Clientbefehlszeichenfolge eine Zeichenfolge enthält, die mit einem **sql** -Abschnittsbezeichner übereinstimmt.

  - Ein **connect** - oder **sql** -Abschnitt mit einem Standardparameter wird verwendet, wenn kein entsprechender Bezeichner vorhanden ist.

  - Ein **userlist** -Abschnitt wird verwendet, wenn der **userlist** -Abschnittsbezeichner mit einem **connect** -Abschnittsbezeichner übereinstimmt. Wenn eine Übereinstimmung vorliegt, wird der Inhalt des **userlist** -Abschnitts auf die Verbindung angewendet, die dem **connect** -Abschnitt unterliegt.

  - Wenn die Zeichenfolge in einer Verbindungs- oder Befehlszeichenfolge nicht mit dem Bezeichner in einem **connect** - oder **sql** -Abschnittsheader übereinstimmt und kein **connect** - oder **sql** -Abschnittsheader mit einem Standardparameter vorhanden ist, wird die Clientzeichenfolge ohne Änderung verwendet.

  - Der **logs** -Abschnitt wird verwendet, wenn **DataFactory** ausgeführt wird.

