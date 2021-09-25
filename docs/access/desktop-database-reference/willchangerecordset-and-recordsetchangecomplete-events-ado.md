---
title: WillChangeRecordset- und RecordsetChangeComplete-Ereignisse (ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a44e86f97b6630e0f2949b0527d6fd4c4fc57622
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614899"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a>WillChangeRecordset- und RecordsetChangeComplete-Ereignisse (ADO)

**Gilt für**: Access 2013, Office 2013

Das **WillChangeRecordset** -Ereignis wird aufgerufen, bevor ein ausstehender Vorgang das [Recordset](recordset-object-ado.md)-Objekt ändert. Das **RecordsetChangeComplete** -Ereignis wird aufgerufen, nachdem das **Recordset** -Objekt geändert wurde.

## <a name="syntax"></a>Syntax

WillChangeRecordset *adReason*, *adStatus*, *pRecordset*

RecordsetChangeComplete *adReason*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*adReason* |Ein [EventReasonEnum](eventreasonenum.md)-Wert, der den Grund für dieses Ereignis angibt. Der Wert kann **adRsnRequery**, **adRsnResynch**, **adRsnClose** oder **adRsnOpen** sein.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Wird **WillChangeRecordset** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann. <br/><br/>Wird **RecordsetChangeComplete** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Er wird auf **adStatusErrorsOccurred** festgelegt, wenn der Vorgang fehlgeschlagen ist. Oder er wird auf **adStatusCancel** festgelegt, wenn der dem zuvor angenommenen **WillChangeRecordset** -Ereignis zugeordnete Vorgang abgebrochen wurde. <br/><br/>Before **WillChangeRecordset** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notifications. <br/><br/>Legen Sie diesen Parameter vor der Rückgabe von **WillChangeRecordset** oder **RecordsetChangeComplete** auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.|
|*Perror* |Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.|
|*pRecordset* |Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.|

## <a name="remarks"></a>Bemerkungen

Ein **WillChangeRecordset-** oder **RecordsetChangeComplete-Ereignis** kann aufgrund der **Methoden Recordset** [Requery](requery-method-ado.md) oder [Open](open-method-ado-recordset.md) auftreten.

Wenn der Anbieter Textmarken nicht unterstützt, tritt immer eine **RecordsetChange** -Ereignisbenachrichtigung auf, wenn neue Zeilen vom Anbieter abgerufen werden. Die Häufigkeit dieses Ereignisses hängt von der **RecordsetCacheSize** -Eigenschaft ab.

Sie müssen den  **adStatus**  -Parameter für jeden möglichen **adReason** -Wert auf **adStatusUnwantedEvent** festlegen, um Ereignisbenachrichtigungen für Ereignisse mit einem  **adReason**  -Parameter vollständig zu beenden.

