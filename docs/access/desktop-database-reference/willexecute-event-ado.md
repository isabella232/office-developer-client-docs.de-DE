---
title: WillExecute-Ereignis (ADO)
TOCTitle: WillExecute event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4d911b46800c0b7b9a45b3697088a4c29c86ec3d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585046"
---
# <a name="willexecute-event-ado"></a>WillExecute-Ereignis (ADO)

**Gilt für**: Access 2013, Office 2013

Das **WillExecute**-Ereignis wird unmittelbar vor dem Ausführen eines ausstehenden Befehls für eine Verbindung aufgerufen.

## <a name="syntax"></a>Syntax

WillExecute *Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Source* |Ein **String** -Wert, der einen SQL-Befehl oder den Namen einer gespeicherten Prozedur enthält.|
|*Cursortype* |Ein [CursorTypeEnum](cursortypeenum.md)-Wert, der den Cursortyp für das **Recordset** -Objekt angibt, dass geöffnet wird. Mit diesem Parameter können Sie den Cursor während eines **Recordset** [Open-Vorgangs](open-method-ado-recordset.md) in einen beliebigen Typ ändern. *CursorType* wird für alle anderen Vorgänge ignoriert.|
|*LockType* |Ein [LockTypeEnum](locktypeenum.md)-Wert, der den Sperrtyp für das **Recordset** -Objekt enthält, das geöffnet wird. Mit diesem Parameter können Sie beim **Open** -Vorgang des **Recordset** -Objekts die Sperre in einen beliebigen Typ ändern. *LockType* wird für alle anderen Vorgänge ignoriert.|
|*Options* |Ein **Long** -Wert, der die Optionen angibt, die zum Ausführen des Befehls oder zum Öffnen des **Recordset** -Objekts verwendet werden können.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Legen Sie diesen Parameter vor Rückgabe des Ereignisses auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern. Oder legen Sie ihn auf **adStatusCancel** fest, um den Abbruch des das Ereignis verursachenden Vorgangs anzufordern.|
|*pCommand* |Das [Command](command-object-ado.md)-Objekt, für das diese Ereignisbenachrichtigung gilt.|
|*pRecordset* |Das [Recordset](recordset-object-ado.md)-Objekt, für das diese Ereignisbenachrichtigung gilt.|
|*pConnection* |Das [Connection](connection-object-ado.md)-Objekt, für das diese Ereignisbenachrichtigung gilt.|

## <a name="remarks"></a>HinwBemerkungeneise

Ein **WillExecute**-Ereignis kann aufgrund einer **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection)-, **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)- oder **Recordset.**[Open](open-method-ado-recordset.md)-Methode eintreten. Der *pConnection*-Parameter sollte immer einen gültigen Verweis auf ein **Connection**-Objekt enthalten. Tritt das Ereignis aufgrund von **Connection.Execute** ein, werden die Parameter *pRecordset* und *pCommand* auf **Nothing** festgelegt. Tritt das Ereignis aufgrund von **Recordset.Open** ein, verweist der *pRecordset*-Parameter auf das **Recordset**-Objekt, und der *pCommand*-Parameter wird auf **Nothing** festgelegt. Tritt das Ereignis aufgrund von **Command.Execute** ein, verweist der *pCommand*-Parameter auf das **Command**-Objekt, und der *pRecordset*-Parameter wird auf **Nothing** festgelegt.

Mit **WillExecute** können Sie die ausstehenden Ausführungsparameter untersuchen und ändern. Dieses Ereignis kann eine Anforderung zurückgeben, dass der ausstehende Befehl abgebrochen wird.

