---
title: WillMove-und MoveComplete-Ereignisse (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e663e18a13803097d490e0e315d139e6e15400da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306055"
---
# <a name="willmove-and-movecomplete-events-ado"></a>WillMove-und MoveComplete-Ereignisse (ADO)

**Gilt für**: Access 2013, Office 2013

Das **WillMove** -Ereignis wird aufgerufen, bevor ein ausstehender Vorgang die aktuelle Position im [Recordset](recordset-object-ado.md)-Objekt ändert. Das **MoveComplete** -Ereignis wird aufgerufen, nachdem die aktuelle Position im **Recordset** -Objekt geändert wurde.

## <a name="syntax"></a>Syntax

WillMove-*Begründung*, *Status*, precordset **

MoveComplete**, *pError*, *Status*, precordset **

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*adReason* |Ein [EventReasonEnum](eventreasonenum.md)-Wert, der den Grund für dieses Ereignis angibt. Der Wert kann **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** oder **adRsnRequery** sein.|
|*pError* |Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Wird **WillMove** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann. <br/><br/>Wird **MoveComplete** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Er wird auf **adStatusErrorsOccurred** festgelegt, wenn der Vorgang fehlgeschlagen ist. <br/><br/>Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications. <br/><br/>Legen Sie diesen Parameter vor der Rückgabe von **MoveComplete** auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.|
|*precordset* |Ein [Recordset](recordset-object-ado.md)-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.|

## <a name="remarks"></a>Bemerkungen

Ein **WillMove** -oder **MoveComplete** -Ereignis kann aufgrund der folgenden **Recordset** -Vorgänge auftreten:

- [Open](open-method-ado-recordset.md)
- [Move](move-method-ado.md)
- [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [AddNew](addnew-method-ado.md)
- [Requery](requery-method-ado.md)

Diese Ereignisse können aufgrund der folgenden Eigenschaften auftreten:

- [Filter](filter-property-ado.md)
- [Index](index-property-ado.md)
- [Bookmark](bookmark-property-ado.md)
- [AbsolutePage](absolutepage-property-ado.md)
- [AbsolutePosition](absoluteposition-property-ado.md)

Diese Ereignisse treten außerdem ein, wenn mit einem untergeordneten **Recordset** -Objekt **Recordset** -Ereignisse verbunden sind und das übergeordnete **Recordset** -Objekt verschoben wird.

Sie müssen den  *adStatus*  -Parameter für jeden möglichen **adReason** -Wert auf *adStatusUnwantedEvent* festlegen, um Ereignisbenachrichtigungen für Ereignisse mit einem  *adReason*  -Parameter vollständig zu beenden.

