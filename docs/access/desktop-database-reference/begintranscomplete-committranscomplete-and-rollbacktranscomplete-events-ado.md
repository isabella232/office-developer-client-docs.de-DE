---
title: BeginTransComplete-, CommitTransComplete-, RollbackTransComplete-Ereignis (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 42379afcc6bb002abaa8cd854eafbc00aa355771
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558758"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a>BeginTransComplete-, CommitTransComplete- und RollbackTransComplete-Ereignisse (ADO)

**Gilt für**: Access 2013, Office 2013

Diese Ereignisse werden aufgerufen, nachdem die zugeordnete Operation für das [Connection](connection-object-ado.md)-Objekt die Ausführung beendet hat.

- **BeginTransComplete** wird nach der [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.

- **CommitTransComplete** wird nach der [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.

- **RollbackTransComplete** wird nach der [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.

## <a name="syntax"></a>Syntax

BeginTransComplete *TransactionLevel*, *pError*, *adStatus*, *pConnection*

CommitTransComplete *pError*, *adStatus*, *pConnection*

RollbackTransComplete *pError*, *adStatus*, *pConnection*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*TransactionLevel* |Ein **Long** -Wert, der die neue Transaktionsebene von **BeginTrans** enthält, das zu diesem Ereignis führte.|
|*Perror* |Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der aufgetreten ist, wenn der Wert von EventStatusEnum **adStatusErrorsOccurred** ist ; andernfalls ist sie nicht festgelegt.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Diese Ereignisse können nachfolgende Benachrichtigungen verhindern, indem dieser Parameter auf **AdStatusUnwantedEvent** festgelegt wird, bevor das Ereignis zurückgegeben wird.|
|*pConnection* |Das **Connection**-Objekt, für das dieses Ereignis auftrat.|

## <a name="remarks"></a>HinwBemerkungeneise

In Visual C++, multiple **Connections** can share the same event handling method. The method uses the returned **Connection** object to determine which object caused the event.

Wenn die [Attributes](attributes-property-ado.md)-Eigenschaft auf **adXactCommitRetaining** oder **adXactAbortRetaining** festgelegt ist, beginnt nach dem Commit oder Rollback eine neue Transaktion. Verwenden Sie das **BeginTransComplete**-Ereignis, um alle Transaktionsstartereignisse, mit Ausnahme des ersten, zu ignorieren.

