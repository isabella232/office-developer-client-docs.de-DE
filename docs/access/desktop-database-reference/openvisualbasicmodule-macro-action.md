---
title: OpenVisualBasicModule-Makroaktion
TOCTitle: OpenVisualBasicModule macro action
ms:assetid: 26eb31c8-3c65-b17d-46cd-c8967434a7a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191906(v=office.15)
ms:contentKeyID: 48543826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50916
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 55af2ce884b26b4c3df219e7d1986e7dc2e4c8ce
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701697"
---
# <a name="openvisualbasicmodule-macro-action"></a>OpenVisualBasicModule-Makroaktion

**Betrifft**: Access 2013, Office 2013

Sie können die **ÖffnenVisualBasicModul** -Aktion verwenden, um ein angegebenes VBA-Modul (Visual Basic für Applikationen) in einer angegebenen Prozedur zu öffnen. Dies kann eine Unterprozedur, eine Funktion oder eine Ereignisprozedur sein.

> [!NOTE]
> [!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **ÖffnenVisualBasicModul** -Aktion hat die folgenden Argumente.

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
<td><p><strong>Modulname</strong></p></td>
<td><p>Der Name des Moduls, den Sie öffnen möchten. Sie können dieses Argument leer lassen, wenn Sie alle Standardmodule in der Datenbank für eine Prozedur durchsuchen, und öffnen Sie das entsprechende Modul bei dieser Prozedur möchten. Wenn Sie ein Makro, das die <strong>ÖffnenVisualBasicModul</strong>-Aktion enthält, in einer Bibliotheksdatenbank ausführen, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Modul mit diesem Namen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Prozedurname</strong></p></td>
<td><p>Der Name der Prozedur, in der das Modul geöffnet werden soll. Wenn Sie für dieses Argument keinen Wert eingeben, wird das Modul im Deklarationsbereich geöffnet.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!HINWEIS] Sie müssen entweder im Argument **Modulname** oder im Argument **Prozedurname** einen gültigen Namen eingeben.


## <a name="remarks"></a>Hinweise

Diese Aktion können Sie eine Ereignisprozedur öffnen, indem Sie das Argument **Modulname** und im Argument **Prozedurname** angeben. Angenommen, Sie zum Öffnen die Ereignisprozedur **Klicken Sie auf** die Schaltfläche Rechnungsdruck auf dem Formular Bestellungen das Argument **Modulname** auf **Form.Orders** festgelegt und die für das Argument **Prozedurname** festlegen **Rechnungsdruck\_klicken Sie auf**. Wenn die Ereignisprozedur für ein Formular oder Bericht anzeigen möchten, muss das Formular oder der Bericht geöffnet sein.

Zum Öffnen einer Prozedur in einem Klassenmodul müssen Sie den Modulnamen entsprechend festlegen, obwohl das Klassenmodul nicht geöffnet werden muss.

Zum Öffnen einer privaten Prozedur muss das Modul, in dem diese Prozedur enthalten ist, geöffnet sein.

Diese Aktion bewirkt dasselbe, wie wenn Sie im Navigationsbereich auf ein Modul doppelklicken und dann auf **Entwurfsansicht** klicken. Mithilfe dieser Aktion können Sie außerdem einen Prozedurnamen angeben und in den Standardmodulen in einer Datenbank nach Prozeduren suchen.

> [!TIP]
> [!TIPP] Sie können ein Modul im Navigationsbereich auswählen und in die Aktionszeile des Makros ziehen. Damit wird automatisch eine **ÖffnenVisualBasicModul** -Aktion erstellt, mit der das Modul im Deklarationsbereich geöffnet wird.

Wenn Sie die **ÖffnenVisualBasicModul** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) ausführen möchten, verwenden Sie die **OpenModule** -Methode des **DoCmd** -Objekts.

