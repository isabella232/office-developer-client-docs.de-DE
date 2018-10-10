---
title: AnzeigenSanduhrzeiger-Makroaktion
TOCTitle: DisplayHourglassPointer Macro Action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 003fb36fc876aa573419b963a9eca6f54332190a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474327"
---
# <a name="displayhourglasspointer-macro-action"></a>AnzeigenSanduhrzeiger-Makroaktion


**Betrifft**: Access 2013 | Office 2013

Mit der **AnzeigenSanduhrzeiger** -Aktion können Sie den Mauszeiger so ändern, dass er in Form einer Sanduhr (oder eines anderen Symbols, das Sie ausgewählt haben) angezeigt wird, während ein Makro ausgeführt wird. Diese Aktion bietet einen visuellen Hinweis darauf, dass ein Makro ausgeführt wird. Dies ist besonders nützlich, wenn die Ausführung einer Makroaktion oder des Makros selbst sehr viel Zeit in Anspruch nimmt.

## <a name="setting"></a>Einstellung

Die **AnzeigenSanduhrzeiger** -Aktion hat das folgende Argument.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktionsargument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Sanduhr</strong></p></td>
<td><p>Klicken Sie im Feld Sanduhr des Abschnitts Aktionsargumente des Bereichs Makro-Generator auf Ja (Anzeige des Symbols) oder auf Nein (Anzeige des normalen Mauszeigers). Die Standardeinstellung ist Ja.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Sie verwenden diese Aktion häufig, wenn Sie das Echo mithilfe der **Echo** -Aktion deaktiviert haben. Wenn Echo deaktiviert ist, unterbricht Access Bildschirm Updates, bis das Makro beendet ist.

Access setzt das Argument **Sanduhr** automatisch auf **Nein** zurück, wenn die Makroausführung beendet ist.


> [!NOTE]
> <UL>
> <LI>
> <P>In Microsoft Windows handelt es sich um das Symbol, das Sie für <STRONG>Ausgelastet</STRONG> im Dialogfeld <STRONG>Eigenschaften von Maus</STRONG> der Windows-Systemsteuerung festgelegt haben. Die Standardeinstellung für alle Windows-Betriebssysteme ist ein animiertes Sanduhrsymbol.</P>
> <LI>
> <P>Wenn Sie möchten, können Sie ein anderes Symbol auswählen.</P></LI></UL>



Verwenden Sie die **Hourglass** -Methode des **DoCmd** -Objekts, um die **AnzeigenSanduhrzeiger** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

