---
title: EndOfRecordset-Ereignis (ADO)
TOCTitle: EndOfRecordset Event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bdef3bdf0a2530fb37c71109d8626808695df8be
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474136"
---
# <a name="endofrecordset-event-ado"></a>EndOfRecordset-Ereignis (ADO)


**Betrifft**: Access 2013 | Office 2013



Das **EndOfRecordset** -Ereignis wird aufgerufen, wenn in eine Zeile nach dem Ende des [Recordsets](recordset-object-ado.md) gewechselt wird.

## <a name="syntax"></a>Syntax

EndOfRecordset*fMoreData*, *AdStatus*, *pCommand*

## <a name="parameters"></a>Parameter

  - *fMoreData*

  - Eine **VARIANT\_BOOL** Wert festlegen Variante\_true ist, gibt das **Recordset**mehr Zeilen hinzugefügt wurden.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Wenn **EndOfRecordset** aufgerufen wird, wird dieser Parameter auf **adStatusOK** festgelegt, falls die Operation, die zu diesem Ereignis führte, erfolgreich war. Er wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch der Operation, die zu diesem Ereignis führte, nicht anfordern kann.
    
    Bevor **EndOfRecordset** zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.

  - *pCommand*

  - Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.

## <a name="remarks"></a>Hinweise

Ein **EndOfRecordset** -Ereignis kann auftreten, wenn die [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Operation fehlschlägt.

Dieser Ereignishandler wird aufgerufen, wenn versucht wird, vielleicht verschieben nach dem Ende des **Recordset** -Objekt als Ergebnis einer **MoveNext**aufrufen. Klicken Sie in diesem Fall konnte Sie jedoch mehr Datensätze aus einer Datenbank abzurufen und sie bis zum Ende des **Recordset-Objekts**anfügen. In diesem Fall Variante festlegen *fMoreData* \_TRUE und aus **EndOfRecordset**zurückgegeben. Rufen Sie dann die **MoveNext** erneut aus, um die neu abgerufenen Datensätze zuzugreifen.

