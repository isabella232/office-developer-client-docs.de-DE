---
title: ExecuteComplete-Ereignis (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f451d61b228d85abb16f5d5e08e0fdd40b1c2d55
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597345"
---
# <a name="executecomplete-event-ado"></a>ExecuteComplete-Ereignis (ADO)

**Gilt für**: Access 2013, Office 2013

Das **ExecuteComplete**-Ereignis wird aufgerufen, nachdem ein Befehl ausgeführt wurde.

## <a name="syntax"></a>Syntax

ExecuteComplete *RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*RecordsAffected* |Ein **Long** -Wert, der die Anzahl von Datensätzen angibt, auf die sich der Befehl auswirkt.|
|*Perror* |Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der **adStatus** -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Bevor dieses Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **adStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.|
|*pCommand* |The [Command](command-object-ado.md) object that was executed. Contains a **Command** object even when calling **Connection.Execute** or **Recordset.Open** without explicitly creating a **Command**, in which cases the **Command** object is created internally by ADO.|
|*pRecordset* |Ein [Recordset](recordset-object-ado.md)-Objekt, das das Ergebnis des ausgeführten Befehls darstellt. Dieses Recordset kann leer sein. Sie sollten dieses **Recordset** -Objekt niemals innerhalb dieses Ereignishandlers zerstören. Andernfalls führt dies zu einer Access-Verletzung, wenn ADO versucht, auf ein Objekt zuzugreifen, das nicht mehr vorhanden ist.|
|*pConnection* |Ein [Connection](connection-object-ado.md)-Objekt. Die Verbindung, über die die Operation ausgeführt wurde.|

## <a name="remarks"></a>HinwBemerkungeneise

Ein **ExecuteComplete**-Ereignis kann aufgrund der Methoden **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md) oder **Recordset.**[NextRecordset](nextrecordset-method-ado.md) auftreten.

