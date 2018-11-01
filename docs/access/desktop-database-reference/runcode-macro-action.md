---
title: RunCode-Makroaktion
TOCTitle: RunCode Macro Action
ms:assetid: cb0625be-4b5d-4927-9b0e-59a6e411b5bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834373(v=office.15)
ms:contentKeyID: 48547706
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98700
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e06d3ebb014cc38b19e37098b217bd072af4434a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870961"
---
# <a name="runcode-macro-action"></a>RunCode-Makroaktion


**Betrifft**: Access 2013, Office 2013

Sie können mit der Aktion **AusführenCode** eine Visual Basic for Applications (VBA)-Funktionsprozedur aufrufen.

## <a name="setting"></a>Einstellungen

Die **AusführenCode** -Aktion hat das folgende Argument.

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
<td><p><strong>Funktionsname</strong></p></td>
<td><p>Der Name der VBA-Funktionsprozedur, die aufgerufen werden soll. Geben Sie die gewünschten Funktionsargumente in Klammern an. Geben Sie den Funktionsnamenn im Feld <strong>Funktionsname</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs "Makro-Generator" ein. Dabei handelt es sich um ein Pflichtargument.  </p>

> [!NOTE]
> <P>Klicken Sie in einer Access-Datenbank (.mdb oder .accdb) auf die Schaltfläche <STRONG>Erstellen</STRONG>, um mithilfe des Ausdrucks-Generators eine Funktion für dieses Argument auszuwählen. Klicken Sie dazu im Ausdrucks-Generator auf die gewünschte Funktion in der Liste.</P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Die benutzerdefinierten Funktionen werden in Microsoft Access-Modulen gespeichert.

Sie müssen Klammern angeben, auch wenn die Funktion, wie im folgenden Beispiel, über keine Argumente verfügt.

`TestFunction()`

Im Gegensatz zu benutzerdefinierten Funktionsnamen für Einstellungen der Ereignis-Eigenschaft verwendet, der Funktionsname im Argument **Funktionsname** nicht mit einem Gleichheitszeichen beginnen (**=**).

Access ignoriert den Rückgabewert der Funktion.


> [!NOTE]
> <P>[!HINWEIS] Sie können eine Funktionsprozedur nicht mit einem Makro aufrufen, wenn der Funktionsname dem Modulnamen entspricht.</P>




> [!TIP]
> <P>[!TIPP] Um eine Sub- oder Ereignis-Prozedur in Visual Basic auszuführen, erstellen Sie eine Funktionsprozedur, die die entsprechende Sub- oder Ereignisprozedur aufruft. Führen Sie die Funktionsprozedur dann mit der Aktion <STRONG>AusführenCode</STRONG> aus.</P>



Beim Aufrufen einer Funktion mit der Aktion **AusführenCode** sucht Access in den Standardmodulen der Datenbank nach einer Funktion mit dem Namen, der im Argument **Funktionsname** angegeben wurde. Wird die Aktion allerdings über einen Menübefehl oder ein Ereignis in einem Formular oder Bericht ausgeführt, sucht Access zuerst in den Klassenmodulen des Formulars bzw. Berichts und erst dann in den Standardmodulen. Die Klassenmodule im Bereich **Module** im Navigationsbereich werden nicht nach der Funktion durchsucht, deren Name im Argument **Funktionsname** angegeben wurde.

Diese Aktion ist nicht in einem VBA-Modul verfügbar. Führen Sie die gewünschte Funktionsprozedur stattdessen direkt in VBA aus.

