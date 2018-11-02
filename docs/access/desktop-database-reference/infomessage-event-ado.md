---
title: InfoMessage-Ereignis (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f3850d57bfcbf61cd5e17456f86dd30812dfde4e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921754"
---
# <a name="infomessage-event-ado"></a>InfoMessage-Ereignis (ADO)


**Betrifft**: Access 2013, Office 2013

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

