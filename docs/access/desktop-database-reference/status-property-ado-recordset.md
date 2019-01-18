---
title: Status-Eigenschaft (ADO-Recordset)
TOCTitle: Status property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4017ff216c17479a69d6d07d0abe51b30fd5e680
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706128"
---
# <a name="status-property-ado-recordset"></a>Status-Eigenschaft (ADO-Recordset)


**Betrifft**: Access 2013, Office 2013

Gibt den Status des aktuellen Datensatzes in Bezug auf Batchaktualisierungen oder andere Massenvorgänge an.

## <a name="return-value"></a>Rückgabewert

Gibt eine Summe aus einem oder mehreren [RecordStatusEnum](recordstatusenum.md)-Werten zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Status** -Eigenschaft, um die ausstehende Änderungen für Datensätze zu ermitteln, die während einer Batchaktualisierung geändert werden. Sie können mit der **Status** -Eigenschaft auch den Status der Datensätze anzeigen, die beispielsweise bei folgenden Massenvorgängen zu Fehlern führen: wenn Sie die Methoden [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) oder [CancelBatch](cancelbatch-method-ado.md) für ein [Recordset](recordset-object-ado.md)-Objekt aufrufen oder wenn Sie die [Filter](filter-property-ado.md)-Eigenschaft für ein **Recordset** -Objekt auf ein Textmarkenarray festlegen. Mit dieser Eigenschaft können Sie den Fehler eines bestimmten Datensatzes ermitteln und beheben.

