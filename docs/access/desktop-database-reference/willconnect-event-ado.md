---
title: WillConnect-Ereignis (ADO)
TOCTitle: WillConnect event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e223eebf5f3fa6c9b4780c6d52fbe41b22b42d5c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588588"
---
# <a name="willconnect-event-ado"></a>WillConnect-Ereignis (ADO)

**Gilt für**: Access 2013, Office 2013

Das **WillConnect**-Ereignis wird aufgerufen, bevor eine Verbindung gestartet wird.

## <a name="syntax"></a>Syntax

WillConnect *ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ConnectionString* |Ein **String** -Wert, der Verbindungsinformationen für die ausstehende Verbindung enthält.|
|*UserID* |Ein **String** -Wert, der einen Benutzernamen für die ausstehende Verbindung enthält.|
|*Password* |Ein **String** -Wert, der ein Kennwort für die ausstehende Verbindung enthält.|
|*Options* |Ein **Long**-Wert, der angibt, wie *ConnectionString* vom Anbieter ausgewertet werden soll. Die einzige Option ist **adAsyncOpen**.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Beim Aufrufen dieses Ereignisses wird dieser Parameter standardmäßig auf **adStatusOK** festgelegt. Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn das Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann.<br/><br/>Legen Sie diesen Parameter vor der Rückgabe dieses Ereignisses auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern. Legen Sie diesen Parameter auf **adStatusCancel** fest, um den Verbindungsvorgang anzufordern, der zum Abbruch dieser Benachrichtigung geführt hat.|
|*pConnection* |Das [Connection](connection-object-ado.md)-Objekt, für das diese Ereignisbenachrichtigung gilt. Vom **WillConnect** -Ereignishandler vorgenommene Änderungen an den Parametern des **Connection** -Objekts haben keine Auswirkungen auf das **Connection** -Objekt.|

## <a name="remarks"></a>HinwBemerkungeneise

Wenn **WillConnect** aufgerufen wird, werden für die Parameter *ConnectionString*, *UserID*, *Password* und *Options* die Werte festgelegt, die durch den dieses Ereignis verursachenden Vorgang (die ausstehende Verbindung) bestimmt wurden. Die Parameter können vor der Rückgabe des Ereignisses geändert werden. Von **WillConnect** kann möglicherweise eine Anforderung zurückgegeben werden, dass die ausstehende Verbindung abgebrochen wird.

Wird dieses Ereignis abgebrochen, wird **ConnectComplete** aufgerufen, wobei für den *adStatus*-Parameter **adStatusErrorsOccurred** festgelegt ist.

