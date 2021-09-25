---
title: WillChangeRecord- und RecordChangeComplete-Ereignisse (ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ab79c961e264e7e83c72f8f81e18d3b7c22f0d71
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557743"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a>WillChangeRecord- und RecordChangeComplete-Ereignisse (ADO)

**Gilt für**: Access 2013, Office 2013

Das **WillChangeRecord** -Ereignis wird aufgerufen, bevor ein oder mehrere Datensätze (Zeilen) im [Recordset](recordset-object-ado.md)-Objekt geändert werden. Das **RecordChangeComplete** -Ereignis wird aufgerufen, nachdem ein oder mehrere Datensätze geändert wurden.

## <a name="syntax"></a>Syntax

WillChangeRecord *adReason*, *cRecords*, *adStatus*, *pRecordset*

RecordChangeComplete *adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*adReason* |Ein [EventReasonEnum](eventreasonenum.md)-Wert, der den Grund für dieses Ereignis angibt. Sein Wert kann **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** oder **adRsnFirstChange** sein.|
|*cRecords* |Ein **Long** -Wert, der die Anzahl sich ändernder (betroffener) Datensätze angibt.|
|*Perror* |Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Wird **WillChangeRecord** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann. <br/><br/>Wird **RecordChangeComplete** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Er wird auf **adStatusErrorsOccurred** festgelegt, wenn der Vorgang fehlgeschlagen ist. <br/><br/>Before **WillChangeRecord** returns, set this parameter to **adStatusCancel** to request cancellation of the operation that caused this event or set this parameter to adStatusUnwantedEvent to prevent subsequent notications. <br/><br/>Legen Sie diesen Parameter vor der Rückgabe von **RecordChangeComplete** auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.|
|*pRecordset* |Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.|

## <a name="remarks"></a>HinwBemerkungeneise

Ein **WillChangeRecord** - oder ein **RecordChangeComplete** -Ereignis kann aufgrund der folgenden **Recordset** -Vorgänge für das erste geänderte Feld einer Zeile eintreten: [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) und [CancelBatch](cancelbatch-method-ado.md). Der Wert des **Recordset** [CursorType](cursortype-property-ado.md) bestimmt, welche Vorgänge die Ereignisse auslösen.

Während des **WillChangeRecord** -Ereignisses wird die **Recordset** [Filter](filter-property-ado.md) -Eigenschaft auf **adFilterAffectedRecords** festgelegt. Sie können diese Eigenschaft nicht ändern, während das Ereignis verarbeitet wird.

You must set the adStatus parameter to adStatusUnwantedEvent for each possible adReason value in order to completely stop event noticiation for any event that includes an adReason parameter.

