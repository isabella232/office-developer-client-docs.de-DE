---
title: EndOfRecordset-Ereignis (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48e0eb25b443175013a144fafaa433df12c2cc9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293560"
---
# <a name="endofrecordset-event-ado"></a>EndOfRecordset-Ereignis (ADO)

**Gilt für**: Access 2013, Office 2013

Das **EndOfRecordset**-Ereignis wird aufgerufen, wenn in eine Zeile nach dem Ende des [Recordsets](recordset-object-ado.md) gewechselt wird.

## <a name="syntax"></a>Syntax

EndOfRecordset*fMoreData*, *Status*, precordset **

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*fMoreData* |Ein **Variant\_** -Wert vom Typ bool, der bei\_Festlegung auf Variant true angibt, dass dem **Recordset**-Objekt weitere Zeilen hinzugefügt wurden.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Wenn **EndOfRecordset** aufgerufen wird, wird dieser Parameter auf **adStatusOK** festgelegt, falls die Operation, die zu diesem Ereignis führte, erfolgreich war. Er wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch der Operation, die zu diesem Ereignis führte, nicht anfordern kann.<br/><br/>Bevor **EndOfRecordset** zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.|
|*precordset* | Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.|

## <a name="remarks"></a>Bemerkungen

Ein **EndOfRecordset** -Ereignis kann auftreten, wenn die [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Operation fehlschlägt.

This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**. However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**. Legen Sie in diesem Fall *fMoreData* auf Variant\_true fest, und geben Sie von **EndOfRecordset**zurück. Then call **MoveNext** again to access the newly retrieved records.

