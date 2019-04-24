---
title: EditMode-Eigenschaft (ADO)
TOCTitle: EditMode property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d7bba0af804df89bf4c8611e184928c9bf12d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293609"
---
# <a name="editmode-property-ado"></a>EditMode-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den Bearbeitungsstatus des aktuellen Datensatzes an.

## <a name="return-value"></a>Rückgabewert

Gibt einen [EditModeEnum](editmodeenum.md)-Wert zurück.

## <a name="remarks"></a>Bemerkungen

ADO verwaltet einen Bearbeitungspuffer, der dem aktuellen Datensatz zugeordnet ist. Diese Eigenschaft gibt an, ob Änderungen an diesem Puffer vorgenommen wurden oder ob ein neuer Datensatz erstellt wurde. Verwenden Sie die **EditMode** -Eigenschaft, um den Bearbeitungsstatus des aktuellen Datensatzes zu bestimmen. Sie können testen, ob ausstehende Änderungen vorhanden sind, falls ein Bearbeitungsprozess unterbrochen wurde, und bestimmen, ob die [Update](update-method-ado.md)- oder die [CancelUpdate](cancelupdate-method-ado.md)-Methode zu verwenden ist.

Eine ausführlichere Beschreibung der [EditMode](addnew-method-ado.md) -Eigenschaft unter verschiedenen Bearbeitungsbedingungen finden Sie unter der **AddNew**-Methode.

Wenn ein Aufruf von [Delete](delete-method-ado-recordset.md) den Datensatz oder die Datensätze in der Datenquelle nicht erfolgreich löscht (beispielsweise aufgrund von Verletzungen der referenziellen Integrität), verbleibt das [Recordset](recordset-object-ado.md) -Objekt im Bearbeitungsmodus (**EditMode** = **adEditInProgress **). Dies bedeutet, dass **CancelUpdate** aufgerufen werden muss, bevor Sie den aktuellen Datensatz verlassen (z. B. mit [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) oder [Close](close-method-ado.md)).


> [!NOTE]
> **EditMode** can return a valid value only if there is a current record. **EditMode** will return an error if [BOF or EOF](bof-eof-properties-ado.md) is true, or if the current record has been deleted.


