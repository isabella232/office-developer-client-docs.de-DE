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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721360"
---
# <a name="endofrecordset-event-ado"></a>EndOfRecordset-Ereignis (ADO)

**Betrifft**: Access 2013, Office 2013

Das **EndOfRecordset** -Ereignis wird aufgerufen, wenn in eine Zeile nach dem Ende des [Recordsets](recordset-object-ado.md) gewechselt wird.

## <a name="syntax"></a>Syntax

EndOfRecordset*fMoreData*, *AdStatus*, *pCommand*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*fMoreData* |Eine **VARIANT\_BOOL** Wert festlegen Variante\_true ist, gibt das **Recordset**mehr Zeilen hinzugefügt wurden.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Wenn **EndOfRecordset** aufgerufen wird, wird dieser Parameter auf **adStatusOK** festgelegt, falls die Operation, die zu diesem Ereignis führte, erfolgreich war. Er wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch der Operation, die zu diesem Ereignis führte, nicht anfordern kann.<br/><br/>Bevor **EndOfRecordset** zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.|
|*pCommand* | Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.|

## <a name="remarks"></a>Hinweise

Ein **EndOfRecordset** -Ereignis kann auftreten, wenn die [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Operation fehlschlägt.

Dieser Ereignishandler wird aufgerufen, wenn versucht wird, vielleicht verschieben nach dem Ende des **Recordset** -Objekt als Ergebnis einer **MoveNext**aufrufen. Klicken Sie in diesem Fall konnte Sie jedoch mehr Datensätze aus einer Datenbank abzurufen und sie bis zum Ende des **Recordset-Objekts**anfügen. In diesem Fall Variante festlegen *fMoreData* \_TRUE und aus **EndOfRecordset**zurückgegeben. Rufen Sie dann die **MoveNext** erneut aus, um die neu abgerufenen Datensätze zuzugreifen.

