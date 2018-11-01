---
title: ExecuteComplete-Ereignis (ADO)
TOCTitle: ExecuteComplete Event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e29db2848d7ec7b229831156ee64815a152a4bfc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887901"
---
# <a name="executecomplete-event-ado"></a>ExecuteComplete-Ereignis (ADO)


**Betrifft**: Access 2013, Office 2013



Das **ExecuteComplete** -Ereignis wird aufgerufen, nachdem ein Befehl ausgeführt wurde.

## <a name="syntax"></a>Syntax

ExecuteComplete*RecordsAffected*, *pError*, *AdStatus*, *pCommand*, *pCommand*, *pConnection*

## <a name="parameters"></a>Parameter

  - *RecordsAffected*

  - Ein **Long** -Wert, der die Anzahl von Datensätzen angibt, auf die sich der Befehl auswirkt.

  - *pError*

  - Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der **adStatus** -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Bevor dieses Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.

  - *pCommand*

  - Das [Command](command-object-ado.md) -Objekt, das ausgeführt wurde. Enthält ein **Command** -Objekt, selbst wenn **Connection.Execute** oder **Recordset.Open** ohne explizit Erstellen eines **Befehls**, in denen Anfragen das **Command** -Objekt von ADO intern erstellt wird.

  - *pCommand*

  - Ein [Recordset](recordset-object-ado.md)-Objekt, das das Ergebnis des ausgeführten Befehls darstellt. Dieses Recordset kann leer sein. Sie sollten dieses **Recordset** -Objekt niemals innerhalb dieses Ereignishandlers zerstören. Andernfalls führt dies zu einer Access-Verletzung, wenn ADO versucht, auf ein Objekt zuzugreifen, das nicht mehr vorhanden ist.

  - *pConnection*

  - Ein [Connection](connection-object-ado.md)-Objekt. Die Verbindung, über die die Operation ausgeführt wurde.

## <a name="remarks"></a>Hinweise

Ein **ExecuteComplete** -Ereignis kann aufgrund der Methoden **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md) oder **Recordset.**[NextRecordset](nextrecordset-method-ado.md) auftreten.

