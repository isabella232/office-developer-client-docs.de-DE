---
title: FetchComplete-Ereignis (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f8c5d775610270ffe2b31a352ac595d5f86008a3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558366"
---
# <a name="fetchcomplete-event-ado"></a>FetchComplete-Ereignis (ADO)

**Gilt für**: Access 2013, Office 2013

Das **FetchComplete**-Ereignis wird aufgerufen, nachdem alle Datensätze in einer langen asynchronen Operation in das [Recordset](recordset-object-ado.md) abgerufen wurden.

## <a name="syntax"></a>Syntax

FetchComplete *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Perror* |Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der **adStatus** -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Bevor dieses Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.|
|*pRecordset* |Ein **Recordset** -Objekt. Das Objekt, für das die Datensätze abgerufen wurden.|

## <a name="remarks"></a>HinwBemerkungeneise

Um **FetchComplete** mit Microsoft Visual Basic zu verwenden, ist Visual Basic 6.0 oder höher erforderlich.

