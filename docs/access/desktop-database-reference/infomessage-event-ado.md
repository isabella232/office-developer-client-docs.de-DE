---
title: InfoMessage-Ereignis (ADO)
TOCTitle: InfoMessage Event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6cc3b69eb3310d8e717605edd3d6fae32d635806
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476041"
---
# <a name="infomessage-event-ado"></a>InfoMessage-Ereignis (ADO)


**Betrifft**: Access 2013 | Office 2013

Das **InfoMessage** -Ereignis wird aufgerufen, wenn eine Warnung während einer **ConnectionEvent** -Operation auftritt.

## <a name="syntax"></a>Syntax

InfoMessage*pError*, *AdStatus*, *pConnection*

## <a name="parameters"></a>Parameter

  - *pError*

  - Ein [Error](error-object-ado.md)-Objekt. Dieser Parameter enthält sämtliche Fehler, die zurückgegeben werden. Wenn mehrere Fehler zurückgegeben werden, zählen Sie die **Fehler** -Auflistung auf, um sie zu finden.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Bevor dieses Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.

  - *pConnection*

  - Ein [Connection](connection-object-ado.md)-Objekt. Die Verbindung, für die die Warnung aufgetreten ist. Warnungen können beispielsweise auftreten, wenn eine **Verbindung** öffnen-Objekt oder das Ausführen eines [Befehls](command-object-ado.md) für eine **Verbindung**.

