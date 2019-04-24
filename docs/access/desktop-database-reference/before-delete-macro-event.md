---
title: Makroereignis "Vor Löschung"
TOCTitle: Before Delete macro event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2b2a4f978a4af2ba79cab7807f0142d35d7d30c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296913"
---
# <a name="before-delete-macro-event"></a>Makroereignis "Vor Löschung"

**Gilt für**: Access 2013, Office 2013

Das Ereignis **Vor Löschung** tritt ein, wenn ein Datensatz gelöscht wird, jedoch bevor der Commit für die Änderung erfolgt ist.

> [!NOTE]
> Das Ereignis **Vor Löschung** ist nur in Datenmakros verfügbar.

## <a name="remarks"></a>Bemerkungen

Mit dem Ereignis **Vor Löschung** führen Sie sämtliche Aktionen vor dem Löschen eines Datensatzes aus. Das Ereignis **Vor Änderung** wird häufig verwendet, um Überprüfungen auszuführen und benutzerdefinierte Fehlermeldungen auszugeben.

Mithilfe der folgenden Syntax können Sie auf einen Wert im zu löschenden Datensatz zugreifen:

`[Old].[Field Name]`

Verwenden Sie die folgende Syntax, um beispielsweise auf den Wert des QuantityInStock-Felds im zu löschenden Datensatz zuzugreifen:

`[Old].[QuantityInStock]`

Am Ende des Ereignisses **Vor Löschung** werden die Werte im zu löschenden Datensatz dauerhaft gelöscht.

You can cancel the **Before Delete** event by using the **RaiseError** action. Wenn ein Fehler ausgelöst wird, werden die Änderungen im **BEFORE DELETE** -Ereignis verworfen.

In der folgenden Tabelle sind Makros ausgeführt, die im Ereignis **Vor Löschung** verwendet werden können.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Befehlstyp</p></th>
<th><p>Befehl</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Programmablauf</p></td>
<td><p><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></p></td>
</tr>
<tr class="even">
<td><p>Programmablauf</p></td>
<td><p><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></p></td>
</tr>
<tr class="odd">
<td><p>Programmablauf</p></td>
<td><p><a href="if-then-else-macro-block.md">Wenn...Dann...Sonst-Makroblock</a></p></td>
</tr>
<tr class="even">
<td><p>Datenblock</p></td>
<td><p><a href="lookuprecord-data-block.md">LookupRecord-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="clearmacroerror-macro-action.md">ClearMacroError-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="onerror-macro-action.md">OnError-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="raiseerror-macro-action.md">RaiseError-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="setlocalvar-macro-action.md">SetLocalVar-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="stopmacro-macro-action.md">StopMacro-Makroaktion</a></p></td>
</tr>
</tbody>
</table>


Zum Erstellen eines Datenmakros, mit dem das Ereignis **Vor Löschung** erfasst wird, führen Sie die folgenden Schritte aus.

1.  Öffnen Sie die Tabelle, für die Sie das Ereignis **Vor Löschung** erfassen möchten.

2.  Wählen Sie auf der Registerkarte **Tabelle** in der Gruppe **before-Ereignisse** **vor löschen**aus.

