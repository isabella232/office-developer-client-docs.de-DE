---
title: Status-Eigenschaft (ADO-Recordset)
TOCTitle: Status Property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1ce4e3fc2d879521bbe1bbdb34d203a640fbe06c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472917"
---
# <a name="status-property-ado-recordset"></a>Status-Eigenschaft (ADO-Recordset)


**Betrifft**: Access 2013 | Office 2013

Gibt den Status des aktuellen Datensatzes in Bezug auf Batchaktualisierungen oder andere Massenvorgänge an.

## <a name="return-value"></a>Rückgabewert

Gibt eine Summe aus einem oder mehreren [RecordStatusEnum](recordstatusenum.md)-Werten zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Status** -Eigenschaft, um die ausstehende Änderungen für Datensätze zu ermitteln, die während einer Batchaktualisierung geändert werden. Sie können mit der **Status** -Eigenschaft auch den Status der Datensätze anzeigen, die beispielsweise bei folgenden Massenvorgängen zu Fehlern führen: wenn Sie die Methoden [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) oder [CancelBatch](cancelbatch-method-ado.md) für ein [Recordset](recordset-object-ado.md)-Objekt aufrufen oder wenn Sie die [Filter](filter-property-ado.md)-Eigenschaft für ein **Recordset** -Objekt auf ein Textmarkenarray festlegen. Mit dieser Eigenschaft können Sie den Fehler eines bestimmten Datensatzes ermitteln und beheben.

