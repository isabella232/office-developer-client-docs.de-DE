---
title: SetProperty-Makroaktion
TOCTitle: SetProperty macro action
ms:assetid: 58d2eac3-35b2-e9f8-47e0-62c9b52f2c24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194340(v=office.15)
ms:contentKeyID: 48545004
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm139044
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 15ad7954c7c6af3f500fad7075deb175905ae667
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621822"
---
# <a name="setproperty-macro-action"></a>SetProperty-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **FestlegenEigenschaft** -Aktion verwenden, um eine Eigenschaft für ein Steuerelement in einem Formular oder Bericht festzulegen.

## <a name="setting"></a>Einstellung

Die **FestlegenEigenschaft**-Aktion verwendet die folgenden Argumente.

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
<td><p>Steuerelementname</p></td>
<td><p>Geben Sie den Namen des Felds oder Steuerelements ein, für das Sie den Eigenschaftswert festlegen möchten. Verwenden Sie lediglich den Namen des Steuerelements, nicht die vollständige Syntax. Lassen Sie das Argument leer, um die Eigenschaft für das aktuelle Formular oder den aktuellen Bericht festzulegen.</p></td>
</tr>
<tr class="even">
<td><p>Eigenschaft</p></td>
<td><p>Wählen Sie die Eigenschaft aus, die Sie festlegen möchten. Der Abschnitt <strong>Hinweise</strong> in diesem Artikel enthält eine Auflistung der Eigenschaften, die mithilfe dieser Aktion festgelegt werden können.</p></td>
</tr>
<tr class="odd">
<td><p>Wert</p></td>
<td><p>Geben Sie den Wert ein, auf den die Eigenschaft festgelegt werden soll. Verwenden Sie für Eigenschaften, deren Werte entweder "Ja" oder "Nein" lauten, <strong>"-1"</strong> für "Ja" und <strong>"0"</strong> für "Nein".</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

- Mithilfe der **FestlegenEigenschaft**-Aktion können Sie die folgenden Eigenschaften eines Steuerelements festlegen: **Aktiviert**, **Sichtbar**, **Gesperrt**, **Links**, **Oben**, **Breite**, **Höhe**, **Textfarbe**, **Hintergrundfarbe** oder **Beschriftung**.

- Wenn Sie einen ungültigen Wert für das Argument ***Wert*** eingeben, tritt kein Fehler auf. Allerdings kann es passieren, dass Access die Eigenschaft in einen anderen Wert ändert. Dies hängt davon ab, wie das Argument interpretiert wird.

- Sie können die **FestlegenEigenschaft** -Aktion nur dann in einem eigenständigen Makro verwenden, wenn eine Aktion vorangeht, mit der das Formular oder der Bericht ausgewählt wird, in dem das Steuerelement enthalten ist, für das Sie die Eigenschaft festlegen. Wenn das Formular oder der Bericht noch nicht geöffnet ist, verwenden Sie zum Öffnen und Auswählen die Aktion **ÖffnenFormular** bzw. **ÖffnenBericht**. Ist das Formular oder der Bericht geöffnet, können Sie es bzw. ihn mit der **AuswählenObjekt** -Aktion auswählen. Legen Sie die Eigenschaft dann mithilfe der **FestlegenEigenschaft** -Aktion fest. Sie müssen das Objekt nicht auswählen, wenn Sie die **FestlegenEigenschaft** -Aktion in einem Makro verwenden, das in ein Steuerelement eingebettet ist, das sich auf demselben Formular oder in demselben Bericht befindet wie das Steuerelement, für das Sie die Eigenschaft festlegen.

- Verwenden Sie die **FestlegenEigenschaft** -Methode des **DoCmd** -Objekts, um die **FestlegenEigenschaft** -Aktion in einem VBA-Modul auszuführen.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie Sie mit der SetProperty-Aktion die Sichtbarkeit des **Textfelds MyTextBox** umschalten.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
