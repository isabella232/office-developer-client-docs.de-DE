---
title: TableDef. CreateProperty-Methode (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 8a92cc64-414e-f33c-1c3e-d1b62c1688c2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197102(v=office.15)
ms:contentKeyID: 48546197
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3018bf8cc9a62cb866b35992e25ecb1f8f41514f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308421"
---
# <a name="tabledefcreateproperty-method-dao"></a>TableDef. CreateProperty-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Erstellt ein neues, benutzerdefiniertes **[Property](property-object-dao.md)** -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . CreateProperty (***Name***, ***Type***, ***value***, ***DDL***)

*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.

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
<td><p><em>Type</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Konstante, die den Datentyp des neuen <strong>Property</strong>-Objekts definiert. Unter der <strong><a href="field-type-property-dao.md">Type</a></strong> -Eigenschaft finden Sie gültige Datentypen.</p></td>
</tr>
<tr class="odd">
<td><p><em>Wert</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Wert, der den ursprünglichen Eigenschaftswert enthält. Details finden Sie unter der <strong><a href="field-value-property-dao.md">value</a></strong> -Eigenschaft.</p></td>
</tr>
<tr class="even">
<td><p><em>DDL</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Wert (Untertyp <strong>Boolean</strong>), der angibt, ob <strong>Property</strong> ein DDL-Objekt ist. Der Standardwert ist <strong>False</strong>. Wenn DDL auf <strong>true</strong>festgelegt ist, können Benutzer dieses <strong>Property-</strong> Objekt nur ändern oder löschen, wenn Sie über die <strong>dbSecWriteDef</strong> -Berechtigung verfügen.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

Eigenschaft

## <a name="remarks"></a>Bemerkungen

Ein benutzerdefiniertes **Property**-Objekt können Sie nur in der **[Properties](properties-collection-dao.md)** -Auflistung eines beständigen Objekts erstellen.

Wenn Sie **CreateProperty** verwenden und einen oder mehrere optionale Teile weglassen, können Sie die entsprechende Eigenschaft mithilfe einer geeigneten Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das Objekt angefügt haben, können Sie dessen Eigenschafteneinstellungen zum Teil ändern. Weitere Informationen hierzu finden Sie in den Themen zur **Name**-, **Type**- und **Value**-Eigenschaft.

Wenn Name auf ein Objekt verweist, das bereits ein Element der Auflistung ist, tritt ein Laufzeitfehler auf, wenn Sie die **[Append](fields-append-method-dao.md)** -Methode verwenden.

Verwenden Sie die [**Delete**](fields-delete-method-dao.md) -Methode für die [**Properties**](properties-collection-dao.md) -Auflistung, um ein benutzerdefiniertes **Property**-Objekt aus der Auflistung zu entfernen. Sie können keine integrierten Eigenschaften löschen.

> [!NOTE]
> Wenn Sie das Argument DDL weglassen, wird standardmäßig false (nicht-DDL) verwendet. Da keine entsprechende DDL-Eigenschaft verfügbar gemacht wird, müssen Sie ein **Property-** Objekt, das Sie von DDL in nicht-DDL ändern möchten, löschen und neu erstellen.


