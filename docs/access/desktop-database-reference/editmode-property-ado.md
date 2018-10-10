---
title: EditMode-Eigenschaft (ADO)
TOCTitle: EditMode Property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a6c8377e0fa0fc2db1ec2d376ee3c8b9f16e8c99
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473354"
---
# <a name="editmode-property-ado"></a>EditMode-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt den Bearbeitungsstatus des aktuellen Datensatzes an.

## <a name="return-value"></a>Rückgabewert

Gibt einen [EditModeEnum](editmodeenum.md)-Wert zurück.

## <a name="remarks"></a>Hinweise

ADO verwaltet einen Bearbeitungspuffer, der dem aktuellen Datensatz zugeordnet ist. Diese Eigenschaft gibt an, ob Änderungen an diesem Puffer vorgenommen wurden oder ob ein neuer Datensatz erstellt wurde. Verwenden Sie die **EditMode** -Eigenschaft, um den Bearbeitungsstatus des aktuellen Datensatzes zu bestimmen. Sie können testen, ob ausstehende Änderungen vorhanden sind, falls ein Bearbeitungsprozess unterbrochen wurde, und bestimmen, ob die [Update](update-method-ado.md)- oder die [CancelUpdate](cancelupdate-method-ado.md)-Methode zu verwenden ist.

Eine ausführlichere Beschreibung der [EditMode](addnew-method-ado.md) -Eigenschaft unter verschiedenen Bearbeitungsbedingungen finden Sie unter der **AddNew**-Methode.

Wenn ein Anruf an [Löschen](delete-method-ado-recordset.md) löscht den Datensatz nicht erfolgreich oder Datensätze in der Datenquelle (aufgrund von referenzielle Integrität Verstöße, beispielsweise), das [Recordset-Objekt](recordset-object-ado.md) im Bearbeitungsmodus bleiben (**EditMode** = **AdEditInProgress **). Dies bedeutet, dass **CancelUpdate** muss, bevor Sie fortfahren aufgerufen werden deaktiviert den aktuellen Datensatz (mit [Verschieben](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md)oder [Schließen](close-method-ado.md), beispielsweise).


> [!NOTE]
> <P><STRONG>EditMode</STRONG> kann nur einen gültigen Wert zurückgeben, wenn ein aktueller Datensatz vorhanden ist. <STRONG>EditMode</STRONG> gibt einen Fehler zurück, wenn <A href="bof-eof-properties-ado.md">BOF oder EOF</A> true ist, oder wenn der aktuelle Datensatz gelöscht wurde.</P>


