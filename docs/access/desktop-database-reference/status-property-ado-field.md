---
title: Status-Eigenschaft (ADO-Feld)
TOCTitle: Status property (ADO Field)
ms:assetid: 7a7b45e8-2934-2e8e-77fa-a4f38272548d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249507(v=office.15)
ms:contentKeyID: 48545795
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 877a7d17b0f5ad9d5b0c16e6ff2497083c5276a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568383"
---
# <a name="status-property-ado-field"></a>Status-Eigenschaft (ADO-Feld)


**Gilt für**: Access 2013, Office 2013

Gibt den Status eines [Field](field-object-ado.md)-Objekts an.

## <a name="return-value"></a>Rückgabewert

Gibt einen [FieldStatusEnum](fieldstatusenum.md)-Wert zurück. Der Standardwert lautet **AdFieldOK**.

## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft gibt für Felder eines [Recordset](recordset-object-ado.md)-Objekts stets **adFieldOK** zurück.

Ergänzungen oder Löschungen in den [Fields](fields-collection-ado.md)-Auflistungen des [Record](record-object-ado.md)-Objekts werden bis zum Aufrufen der [Update](update-method-ado.md)-Methode zwischengespeichert. Mithilfe der **Status** -Eigenschaft können Sie die Felder ermitteln, die erfolgreich hinzugefügt oder gelöscht wurden.

To enhance performance, schema changes are cached until **Update** is called, and then the changes are made in a batch optimistic update. If the **Update** method is not called, the server is not updated. If any updates fail then an error is returned and the **Status** property indicates the combined values of the operation and error status code. For example, **adFieldPendingInsert** **OR** **adFieldPermissionDenied**. The **Status** property for each **Field** can be used to determine why the **Field** was not added, modified, or deleted. **Status** wird nur für den **Datensatz** sinnvoll verfügbar gemacht. **Fields-Auflistung** und nicht das **Recordset -Objekt.** **Fields-Auflistung.**

Two problems can arise when adding, modifying, or deleting a **Field**. If the user deletes a **Field**, it is marked for deletion from the **Fields** collection. If the subsequent **Update** returns an error because the user tried to delete a **Field** for which they do not have permission, the **Field** will have a status of **adFieldPermissionDenied** **OR** **adFieldPendingDelete**. Calling the [CancelUpdate](cancelupdate-method-ado.md) method restores original values and sets the **Status** to **adFieldOK**. Similarly, the **Update** method may return an error because a new **Field** was added and given an inappropriate value. In that case the new **Field** will be in the **Fields** collection and have a status of **adFieldPendingInsert** and perhaps **adFieldCantCreate**. You can supply an appropriate value for the new **Field** and call **Update** again. Note that calling **Resync** instead requeries the provider.

