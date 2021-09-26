---
title: Status-Eigenschaft (ADO-Recordset)
TOCTitle: Status property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ef2978d699021ebfa0fad6f207778caa019d32b0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621759"
---
# <a name="status-property-ado-recordset"></a>Status-Eigenschaft (ADO-Recordset)


**Gilt für**: Access 2013, Office 2013

Gibt den Status des aktuellen Datensatzes in Bezug auf Batchaktualisierungen oder andere Massenvorgänge an.

## <a name="return-value"></a>Rückgabewert

Gibt eine Summe aus einem oder mehreren [RecordStatusEnum](recordstatusenum.md)-Werten zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Status**-Eigenschaft, um die ausstehende Änderungen für Datensätze zu ermitteln, die während einer Batchaktualisierung geändert werden. Sie können mit der **Status**-Eigenschaft auch den Status der Datensätze anzeigen, die beispielsweise bei folgenden Massenvorgängen zu Fehlern führen: wenn Sie die Methoden [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) oder [CancelBatch](cancelbatch-method-ado.md) für ein [Recordset](recordset-object-ado.md)-Objekt aufrufen oder wenn Sie die [Filter](filter-property-ado.md)-Eigenschaft für ein **Recordset**-Objekt auf ein Textmarkenarray festlegen. Mit dieser Eigenschaft können Sie den Fehler eines bestimmten Datensatzes ermitteln und beheben.

