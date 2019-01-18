---
title: WillConnect-Ereignis (ADO)
TOCTitle: WillConnect event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e62a01d274752b33f7bf3f6f4af6171e7efb16b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703433"
---
# <a name="willconnect-event-ado"></a>WillConnect-Ereignis (ADO)

**Betrifft**: Access 2013, Office 2013

Das **WillConnect** -Ereignis wird aufgerufen, bevor eine Verbindung gestartet wird.

## <a name="syntax"></a>Syntax

WillConnect*ConnectionString*, *UserID*, *Kennwort*, *Optionen*, *AdStatus*, *pConnection*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ConnectionString* |Ein **String** -Wert, der Verbindungsinformationen für die ausstehende Verbindung enthält.|
|*UserID* |Ein **String** -Wert, der einen Benutzernamen für die ausstehende Verbindung enthält.|
|*Password* |Ein **String** -Wert, der ein Kennwort für die ausstehende Verbindung enthält.|
|*Options* |Ein **Long**-Wert, der angibt, wie *ConnectionString* vom Anbieter ausgewertet werden soll. Die einzige Option ist **adAsyncOpen**.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Beim Aufrufen dieses Ereignisses wird dieser Parameter standardmäßig auf **adStatusOK** festgelegt. Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn das Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann.<br/><br/>Legen Sie diesen Parameter vor der Rückgabe dieses Ereignisses auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern. Legen Sie diesen Parameter auf **adStatusCancel** fest, um den Verbindungsvorgang anzufordern, der zum Abbruch dieser Benachrichtigung geführt hat.|
|*pConnection* |Das [Connection](connection-object-ado.md)-Objekt, für das diese Ereignisbenachrichtigung gilt. Vom **WillConnect** -Ereignishandler vorgenommene Änderungen an den Parametern des **Connection** -Objekts haben keine Auswirkungen auf das **Connection** -Objekt.|

## <a name="remarks"></a>Hinweise

Wenn **WillConnect** aufgerufen wird, werden für die Parameter *ConnectionString*, *UserID*, *Password* und *Options* die Werte festgelegt, die durch den dieses Ereignis verursachenden Vorgang (die ausstehende Verbindung) bestimmt wurden. Die Parameter können vor der Rückgabe des Ereignisses geändert werden. Von **WillConnect** kann möglicherweise eine Anforderung zurückgegeben werden, dass die ausstehende Verbindung abgebrochen wird.

Wenn dieses Ereignis abgebrochen wird, wird mit den *AdStatus* -Parameter auf **AdStatusErrorsOccurred**festgelegt **ConnectComplete** aufgerufen werden.

