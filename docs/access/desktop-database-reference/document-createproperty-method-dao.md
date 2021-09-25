---
title: Document.CreateProperty-Methode (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 834fda60-1edf-38df-a9a5-d9d15e55e425
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196739(v=office.15)
ms:contentKeyID: 48546003
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052967
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 1ed56d43d68de1da03a2bcf47396547951c1b4b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569062"
---
# <a name="documentcreateproperty-method-dao"></a>Document.CreateProperty-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Erstellt ein neues, benutzerdefiniertes **[Property](property-object-dao.md)** -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . CreateProperty(***Name** _, _*_Type_*_, _*_Value_*_, _*_DDL_**)

*Ausdruck* Eine Variable, die ein **Document-Objekt** darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>String</strong>-Wert, der das neue <strong>Property</strong>-Objekt eindeutig benennt. Weitere Informationen zu gültigen <strong>Property</strong>-Namen finden Sie in dem Thema zur <strong>Name</strong>-Eigenschaft.</p></td>
</tr>
<tr class="even">
<td><p><em>Typ</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Konstante, die den Datentyp des neuen <strong>Property</strong>-Objekts definiert. Informationen zu gültigen Datentypen finden Sie in dem Thema zur <strong><a href="field-type-property-dao.md">Type</a></strong>-Eigenschaft.</p></td>
</tr>
<tr class="odd">
<td><p><em>Wert</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Wert, der den ursprünglichen Eigenschaftswert enthält. Weitere Informationen finden Sie in dem Thema zur <strong><a href="field-value-property-dao.md">Value</a></strong>-Eigenschaft.</p></td>
</tr>
<tr class="even">
<td><p><em>DDL</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Wert (Untertyp <strong>Boolean</strong>), der angibt, ob <strong>Property</strong> ein DDL-Objekt ist. Der Standardwert ist <strong>False</strong>. Wenn DDL <strong>"True"</strong>ist, können Benutzer dieses <strong>Property-Objekt</strong> nur dann ändern oder löschen, wenn sie über <strong>die Berechtigung "dbSecWriteDef"</strong> verfügen.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

Eigenschaft

## <a name="remarks"></a>HinwBemerkungeneise

Ein benutzerdefiniertes **Property**-Objekt können Sie nur in der **[Properties](properties-collection-dao.md)** -Auflistung eines beständigen Objekts erstellen.

Wenn Sie **CreateProperty** verwenden und einen oder mehrere optionale Teile weglassen, können Sie die entsprechende Eigenschaft mithilfe einer geeigneten Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das Objekt angefügt haben, können Sie dessen Eigenschafteneinstellungen zum Teil ändern. Weitere Informationen hierzu finden Sie in den Themen zur **Name**-, **Type**- und **Value**-Eigenschaft.

Wenn sich der Name auf ein Objekt bezieht, das bereits ein Element der Auflistung ist, tritt ein Laufzeitfehler auf, wenn Sie die **[Append-Methode](fields-append-method-dao.md)** verwenden.

Um ein benutzerdefiniertes **Property** -Objekt aus der Auflistung zu entfernen, verwenden Sie die **[Delete](fields-delete-method-dao.md)** -Methode für die **Properties -Auflistung.** Sie können keine integrierten Eigenschaften löschen.


> [!NOTE]
> Wenn Sie das Argument DDL weglassen, wird standardmäßig False (nicht DDL) verwendet. Da keine entsprechende DDL-Eigenschaft verfügbar gemacht wurde, müssen Sie ein **Property**-Objekt, das von DLL in Nicht-DLL geändert werden soll, löschen und erneut erstellen.


