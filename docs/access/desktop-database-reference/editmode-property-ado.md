---
title: EditMode-Eigenschaft (ADO)
TOCTitle: EditMode property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 50fe7a1c034e1e60863ee04da523f41bb7eadb46
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581406"
---
# <a name="editmode-property-ado"></a>EditMode-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den Bearbeitungsstatus des aktuellen Datensatzes an.

## <a name="return-value"></a>Rückgabewert

Gibt einen [EditModeEnum](editmodeenum.md)-Wert zurück.

## <a name="remarks"></a>HinwBemerkungeneise

ADO verwaltet einen Bearbeitungspuffer, der dem aktuellen Datensatz zugeordnet ist. Diese Eigenschaft gibt an, ob Änderungen an diesem Puffer vorgenommen wurden oder ob ein neuer Datensatz erstellt wurde. Verwenden Sie die **EditMode** -Eigenschaft, um den Bearbeitungsstatus des aktuellen Datensatzes zu bestimmen. Sie können testen, ob ausstehende Änderungen vorhanden sind, falls ein Bearbeitungsprozess unterbrochen wurde, und bestimmen, ob die [Update](update-method-ado.md)- oder die [CancelUpdate](cancelupdate-method-ado.md)-Methode zu verwenden ist.

Eine ausführlichere Beschreibung der [EditMode](addnew-method-ado.md) -Eigenschaft unter verschiedenen Bearbeitungsbedingungen finden Sie unter der **AddNew**-Methode.

Wenn ein Aufruf von [Delete](delete-method-ado-recordset.md) den Datensatz oder die Datensätze in der Datenquelle nicht erfolgreich löscht (z. B. aufgrund von Verletzungen der referenziellen Integrität), verbleibt das [Recordset](recordset-object-ado.md) im Bearbeitungsmodus (**EditMode**  =  **adEditInProgress**). Dies bedeutet, dass **CancelUpdate** aufgerufen werden muss, bevor Sie den aktuellen Datensatz verlassen (z. B. mit [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) oder [Close](close-method-ado.md)).


> [!NOTE]
> **EditMode** can return a valid value only if there is a current record. **EditMode** will return an error if [BOF or EOF](bof-eof-properties-ado.md) is true, or if the current record has been deleted.


