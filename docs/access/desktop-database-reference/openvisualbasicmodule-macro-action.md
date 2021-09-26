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
ms.localizationpriority: medium
ms.openlocfilehash: 0474df0c026385731a13bf122c87bebab7af9e3c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626246"
---
# <a name="openvisualbasicmodule-macro-action"></a>OpenVisualBasicModule-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **ÖffnenVisualBasicModul** -Aktion verwenden, um ein angegebenes VBA-Modul (Visual Basic für Applikationen) in einer angegebenen Prozedur zu öffnen. Dies kann eine Unterprozedur, eine Funktion oder eine Ereignisprozedur sein.

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **ÖffnenVisualBasicModul**-Aktion hat die folgenden Argumente.

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
<td><p>Der Name des Moduls, das Sie öffnen möchten. Sie müssen für dieses Argument keinen Wert anzugeben, wenn Sie in allen Standardmodulen in der Datenbank nach einer Prozedur suchen und das entsprechende Modul in dieser Prozedur öffnen möchten. Wenn Sie ein Makro, das die <strong>ÖffnenVisualBasicModul</strong>-Aktion enthält, in einer Bibliotheksdatenbank ausführen, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Modul mit diesem Namen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Prozedurname</strong></p></td>
<td><p>Der Name der Prozedur, in der das Modul geöffnet werden soll. Wenn Sie für dieses Argument keinen Wert eingeben, wird das Modul im Deklarationsbereich geöffnet.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Sie müssen entweder im Argument **Modulname** oder im Argument **Prozedurname** einen gültigen Namen eingeben.


## <a name="remarks"></a>Bemerkungen

You can use this action to open an event procedure by specifying the **Module Name** argument and the **Procedure Name** argument. Um beispielsweise die  Click-Ereignisprozedur der Schaltfläche PrintInvoice auf dem Formular Orders zu öffnen, legen Sie das Argument **Modulname** auf **Form.Orders** fest, und legen Sie das **Argument Prozedurname** auf **PrintInvoice \_ Click** fest. To view the event procedure for a form or report, the form or report must be open.

Zum Öffnen einer Prozedur in einem Klassenmodul müssen Sie den Modulnamen entsprechend festlegen, obwohl das Klassenmodul nicht geöffnet werden muss.

Zum Öffnen einer privaten Prozedur muss das Modul, in dem diese Prozedur enthalten ist, geöffnet sein.

Diese Aktion bewirkt dasselbe, wie wenn Sie im Navigationsbereich auf ein Modul doppelklicken und dann auf **Entwurfsansicht** klicken. Mithilfe dieser Aktion können Sie außerdem einen Prozedurnamen angeben und in den Standardmodulen in einer Datenbank nach Prozeduren suchen.

> [!TIP]
> [!TIPP] Sie können ein Modul im Navigationsbereich auswählen und in die Aktionszeile des Makros ziehen. Damit wird automatisch eine **ÖffnenVisualBasicModul** -Aktion erstellt, mit der das Modul im Deklarationsbereich geöffnet wird.

Wenn Sie die **ÖffnenVisualBasicModul** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) ausführen möchten, verwenden Sie die **OpenModule** -Methode des **DoCmd** -Objekts.

