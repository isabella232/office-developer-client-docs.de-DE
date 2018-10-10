---
title: AusführenMakro-Makroaktion
TOCTitle: RunMacro Macro Action
ms:assetid: 25966f20-8160-0821-b88a-ed08b7786fdc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191868(v=office.15)
ms:contentKeyID: 48543787
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm43195
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 533ac6aff194296a9e4470e01672a8338dcbc318
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475759"
---
# <a name="runmacro-macro-action"></a>AusführenMakro-Makroaktion


**Betrifft**: Access 2013 | Office 2013

Zum Ausführen eines Makros können Sie die **AusführenMakro** -Aktion verwenden. Das Makro kann sich in einer Makrogruppe befinden.

Sie können diese Aktion für Folgendes verwenden:

  - Zum Ausführen eines Makros innerhalb eines anderen Makros.

  - Zum Ausführen eines Makros basierend auf einer bestimmten Bedingung.

  - Zum Anfügen eines Makros an einen benutzerdefinierten Menübefehl.

## <a name="setting"></a>Einstellung

Die **AusführenMakro** -Aktion hat die folgenden Argumente.

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
<td><p><strong>Makroname</strong></p></td>
<td><p>Der Name des auzuführenden Makros. Das Feld <strong>Makroname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators zeigt alle Makros (und Makrogruppen) in der aktuellen Datenbank. Wenn das Makro in einer Makrogruppe befindet, wird sie als <em>Makrogruppenname</em>unter dem Makrogruppennamen in der Liste aufgeführt. <em>Makroname</em>. Dies ist ein erforderliches Argument. Wenn Sie ein Makro ausführen, das die <strong>AusführenMakro</strong>-Aktion in einer Bibliotheksdatenbank enthält, sucht Microsoft Access zunächst in der Bibliotheksdatenbank nach dem Makro mit diesem Namen und dann in der aktuellen Datenbank.</p></td>
</tr>
<tr class="even">
<td><p><strong>Wiederholungen</strong></p></td>
<td><p>Gibt an, wie oft das Makro maximal ausgeführt wird. Wenn Sie dieses Argument leer lassen (und das Argument <strong>Wiederholungen</strong> auch leer ist), wird das Makro einmal ausgeführt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Wiederholbedingung</strong></p></td>
<td><p>Ein Ausdruck, der mit <strong>Wahr</strong> (-1) oder <strong>Falsch</strong> (0) ausgewertet wird. Das Makro beendet die Ausführung des Makros, wenn der Ausdruck als <strong>Falsch</strong> ausgewertet wird. Der Ausdruck wird bei jeder Makroausführung ausgewertet.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Wenn Sie einen Makrogruppennamen für das Argument **Makroname** eingeben, wird das erste Makro in der Makrogruppe in Access ausgeführt.

Diese Aktion ist mit dem Klicken auf **Makro ausführen** auf der Registerkarte **Datenbanktools**, dem Auswählen eines Makros und dem Klicken auf **OK** vergleichbar. Bei diesem Befehl wird das Makro jedoch nur einmal ausgeführt, wohingegen die **AusführenMakro** -Aktion ein Makro so häufig wie gewünscht ausführen kann.


> [!TIP]
> <P>[!TIPP] Sie können die Argumente <STRONG>Wiederholbedingung</STRONG> und <STRONG>Wiederholungen</STRONG> verwenden, um festzulegen, wie oft das Makro ausgeführt wird:</P>



  - Wenn Sie beide Argumente leer lassen, wird das Makro einmal ausgeführt.

  - Wenn Sie einen Wert für **Wiederholungen** eingeben, aber **Wiederholbedingung** leer lassen, wird das Makro mit der angegebenen Häufigkeit ausgeführt.

  - Wenn Sie **Wiederholungen** leer lassen, jedoch einen Ausdruck für **Wiederholbedingung** eingeben, wird das Makro ausgeführt, bis der Ausdruck mit **Falsch** ausgewertet wird.

  - Wenn Sie Werte für beide Argumente eingeben, wird das Makro mit der Häufigkeit ausgeführt, die in **Wiederholungen** angegeben ist, oder bis **Wiederholbedingung** mit **Falsch** ausgewertet wird, unabhängig davon, was zuerst erfolgt.

Wenn Sie ein Makro ausführen, das die **AusführenMakro** -Aktion enthält, und es die **AusführenMakro** -Aktion erreicht, wird das aufgerufene Makro in Access ausgeführt. Sobald das aufgerufene Makro beendet ist, kehrt Access zum ursprünglichen Makro zurück und führt die nächste Aktion aus.


> [!NOTE]
> <UL>
> <LI>
> <P>Sie können ein Makro in derselben Makrogruppe oder in einer anderen Makrogruppe aufrufen.</P>
> <LI>
> <P>Sie können Makros schachteln. Sie können also Makro A ausführen, das wiederum Makro B aufruft usw. Sobald das aufgerufene Makro beendet ist, kehrt Access zu dem Makro zurück, das es aufrief, und führt die nächste Aktion in diesem Makro aus.</P></LI></UL>



Verwenden Sie die **RunMacro** -Methode des **DoCmd** -Objekts, um die **AusführenMakro** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

