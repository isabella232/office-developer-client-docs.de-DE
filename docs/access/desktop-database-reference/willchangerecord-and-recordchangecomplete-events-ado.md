---
title: WillChangeRecord- und RecordChangeComplete-Ereignisse (ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4488b18d6c3ab603a84822bfeea732931746b3be
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949950"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a>WillChangeRecord- und RecordChangeComplete-Ereignisse (ADO)

**Betrifft**: Access 2013, Office 2013

Das **WillChangeRecord** -Ereignis wird aufgerufen, bevor ein oder mehrere Datensätze (Zeilen) im [Recordset](recordset-object-ado.md)-Objekt geändert werden. Das **RecordChangeComplete** -Ereignis wird aufgerufen, nachdem ein oder mehrere Datensätze geändert wurden.

## <a name="syntax"></a>Syntax

WillChangeRecord-*AdReason*, *cRecords*, *AdStatus*, *pCommand*

RecordChangeComplete*AdReason*, *cRecords*, *pError*, *AdStatus*, *pCommand*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*adReason* |Ein [EventReasonEnum](eventreasonenum.md)-Wert, der den Grund für dieses Ereignis angibt. Sein Wert kann **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** oder **adRsnFirstChange** sein.|
|*cRecords* |Ein **Long** -Wert, der die Anzahl sich ändernder (betroffener) Datensätze angibt.|
|*pError* |Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Wird **WillChangeRecord** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann. <br/><br/>Wird **RecordChangeComplete** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Er wird auf **adStatusErrorsOccurred** festgelegt, wenn der Vorgang fehlgeschlagen ist. <br/><br/>Legen Sie diesen Parameter vor der Rückgabe von WillChangeRecord auf adStatusCancel fest, um den Abbruch des dieses Ereignis verursachenden Vorgangs anzufordern. Oder legen Sie diesen Parameter auf adStatusUnwantedEvent fest, um nachfolgende Benachrichtigungen zu verhindern. <br/><br/>Legen Sie diesen Parameter vor der Rückgabe von **RecordChangeComplete** auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.|
|*pCommand* |Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.|

## <a name="remarks"></a>Hinweise

Ein **WillChangeRecord** - oder ein **RecordChangeComplete** -Ereignis kann aufgrund der folgenden **Recordset** -Vorgänge für das erste geänderte Feld einer Zeile eintreten: [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) und [CancelBatch](cancelbatch-method-ado.md). Der Wert der das **Recordset** [CursorType](cursortype-property-ado.md) bestimmt, welche Vorgänge dazu führen, dass die Ereignisse eintritt.

Während des **WillChangeRecord** -Ereignisses wird die **Recordset** - [Filter](filter-property-ado.md) -Eigenschaft auf **AdFilterAffectedRecords**festgelegt. Sie können diese Eigenschaft nicht ändern, während das Ereignis verarbeitet wird.

Sie müssen den adStatus-Parameter für jeden möglichen adReason-Wert auf adStatusUnwantedEvent festlegen, um Ereignisbenachrichtigungen für Ereignisse mit einem adReason-Parameter vollständig zu beenden.

