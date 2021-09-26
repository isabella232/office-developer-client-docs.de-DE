---
title: InfoMessage-Ereignis (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3a629511b87a182d659cba74de537edd15d27b5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631965"
---
# <a name="infomessage-event-ado"></a>InfoMessage-Ereignis (ADO)

**Gilt für**: Access 2013, Office 2013

Das **InfoMessage**-Ereignis wird aufgerufen, wenn eine Warnung während einer **ConnectionEvent**-Operation auftritt.

## <a name="syntax"></a>Syntax

InfoMessage *pError*, *adStatus*, *pConnection*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Perror* |Ein [Error](error-object-ado.md)-Objekt. Dieser Parameter enthält sämtliche Fehler, die zurückgegeben werden. Wenn mehrere Fehler zurückgegeben werden, zählen Sie die **Fehler** -Auflistung auf, um sie zu finden.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Bevor dieses Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.|
|*pConnection* |A [Connection](connection-object-ado.md) object. The connection for which the warning occurred. For example, warnings can occur when opening a **Connection** object or executing a [Command](command-object-ado.md) on a **Connection**.|

