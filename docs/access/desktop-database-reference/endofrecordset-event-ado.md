---
title: EndOfRecordset-Ereignis (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 336dd8f5dce734e7b820f8bf78f113d122d90444
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602752"
---
# <a name="endofrecordset-event-ado"></a>EndOfRecordset-Ereignis (ADO)

**Gilt für**: Access 2013, Office 2013

Das **EndOfRecordset**-Ereignis wird aufgerufen, wenn in eine Zeile nach dem Ende des [Recordsets](recordset-object-ado.md) gewechselt wird.

## <a name="syntax"></a>Syntax

EndOfRecordset *fMoreData*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*fMoreData* |Ein **VARIANT \_ BOOL-Wert,** der, wenn er auf VARIANT TRUE festgelegt \_ ist, angibt, dass dem **Recordset** weitere Zeilen hinzugefügt wurden.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Wenn **EndOfRecordset** aufgerufen wird, wird dieser Parameter auf **adStatusOK** festgelegt, falls die Operation, die zu diesem Ereignis führte, erfolgreich war. Er wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch der Operation, die zu diesem Ereignis führte, nicht anfordern kann.<br/><br/>Bevor **EndOfRecordset** zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.|
|*pRecordset* | Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.|

## <a name="remarks"></a>HinwBemerkungeneise

Ein **EndOfRecordset** -Ereignis kann auftreten, wenn die [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Operation fehlschlägt.

This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**. However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**. Legen Sie in diesem Fall *fMoreData* auf VARIANT \_ TRUE fest, und kehren Sie von **EndOfRecordset** zurück. Then call **MoveNext** again to access the newly retrieved records.

