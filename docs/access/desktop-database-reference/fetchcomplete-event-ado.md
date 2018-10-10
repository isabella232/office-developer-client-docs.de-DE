---
title: FetchComplete-Ereignis (ADO)
TOCTitle: FetchComplete Event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 299fec4a831bbde5d3fd2d58e0f76edb2acea0f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474720"
---
# <a name="fetchcomplete-event-ado"></a>FetchComplete-Ereignis (ADO)


**Betrifft**: Access 2013 | Office 2013


Das **FetchComplete** -Ereignis wird aufgerufen, nachdem alle Datensätze in einer langen asynchronen Operation in das [Recordset](recordset-object-ado.md) abgerufen wurden.

## <a name="syntax"></a>Syntax

FetchComplete*pError*, *AdStatus*, *pCommand*

## <a name="parameters"></a>Parameter

  - *pError*

  - Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der **adStatus** -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Bevor dieses Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.

  - *pCommand*

  - Ein **Recordset** -Objekt. Das Objekt, für das die Datensätze abgerufen wurden.

## <a name="remarks"></a>Hinweise

Um **FetchComplete** mit Microsoft Visual Basic zu verwenden, ist Visual Basic 6.0 oder höher erforderlich.

