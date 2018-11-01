---
title: BeginTransComplete-, CommitTransComplete, RollbackTransComplete-Ereignisse (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bf38a106a8cb53c1603628f0c3c0096be4b73d52
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888636"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a>BeginTransComplete-, CommitTransComplete- und RollbackTransComplete-Ereignisse (ADO)


**Betrifft**: Access 2013, Office 2013


Diese Ereignisse werden aufgerufen, nachdem die zugeordnete Operation für das [Connection](connection-object-ado.md)-Objekt die Ausführung beendet hat.

  - **BeginTransComplete** wird nach der [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.

  - **CommitTransComplete** wird nach der [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.

  - **RollbackTransComplete** wird nach der [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Operation aufgerufen.

## <a name="syntax"></a>Syntax

BeginTransComplete-*TransactionLevel*, *pError*, *AdStatus*, *pConnection*

CommitTransComplete-*pError*, *AdStatus*, *pConnection*

RollbackTransComplete*pError*, *AdStatus*, *pConnection*

## <a name="parameters"></a>Parameter

  - *TransactionLevel*

  - Ein **Long** -Wert, der die neue Transaktionsebene von **BeginTrans** enthält, das zu diesem Ereignis führte.

  - *pError*

  - Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der Wert von EventStatusEnum **adStatusErrorsOccurred** lautet; andernfalls wird er nicht festgelegt.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Diese Ereignisse können nachfolgende Benachrichtigungen verhindern, indem dieser Parameter auf **AdStatusUnwantedEvent** festgelegt wird, bevor das Ereignis zurückgegeben wird.

  - *pConnection*

  - Das **Connection** -Objekt, für das dieses Ereignis auftrat.

## <a name="remarks"></a>Hinweise

In Visual C++ können mehrere **Verbindungen** gleichen Ereignisbehandlung Methode freigeben. Die-Methode verwendet das zurückgegebene **Connection** -Objekt, um zu bestimmen, welches Objekt das Ereignis ausgelöst hat.

Wenn die [Attributes](attributes-property-ado.md)-Eigenschaft auf **adXactCommitRetaining** oder **adXactAbortRetaining** festgelegt ist, beginnt nach dem Commit oder Rollback eine neue Transaktion. Verwenden Sie das **BeginTransComplete** -Ereignis, um alle Transaktionsstartereignisse, mit Ausnahme des ersten, zu ignorieren.

