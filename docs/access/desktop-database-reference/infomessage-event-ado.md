---
title: InfoMessage-Ereignis (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 879d8e7b3733937687671a164f86dbb273cf7533
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291442"
---
# <a name="infomessage-event-ado"></a>InfoMessage-Ereignis (ADO)

**Gilt für**: Access 2013, Office 2013

Das **InfoMessage**-Ereignis wird aufgerufen, wenn eine Warnung während einer **ConnectionEvent**-Operation auftritt.

## <a name="syntax"></a>Syntax

InfoMessage*pError*, ** *pConnection*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*pError* |Ein [Error](error-object-ado.md)-Objekt. Dieser Parameter enthält sämtliche Fehler, die zurückgegeben werden. Wenn mehrere Fehler zurückgegeben werden, zählen Sie die **Fehler** -Auflistung auf, um sie zu finden.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Bevor dieses Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.|
|*pConnection* |A [Connection](connection-object-ado.md) object. The connection for which the warning occurred. For example, warnings can occur when opening a **Connection** object or executing a [Command](command-object-ado.md) on a **Connection**.|

