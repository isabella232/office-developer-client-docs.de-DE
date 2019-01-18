---
title: onError-Ereignis (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712176"
---
# <a name="onerror-event-rds"></a>onError-Ereignis (RDS)

**Betrifft**: Access 2013, Office 2013

Wenn während eines Vorgangs ein Fehler auftritt, wird das **OnError** -Ereignis aufgerufen.

## <a name="syntax"></a>Syntax

OnError*SCode*, *Beschreibung*, *Source*, *CancelDisplay*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*SCode* |Eine ganze Zahl, die den Statuscode des Fehlers angibt.|
|*Description* |Eine **Zeichenfolge** , die eine Beschreibung des Fehlers angibt.|
|*Quelle* |Eine **Zeichenfolge** , die angibt, die Abfrage oder den Befehl, der den Fehler verursacht hat.|
|*CancelDisplay* |Ein **boolescher** Wert, die bei auf **True**festgelegt, die verhindert, dass den Fehler in einem Dialogfeld angezeigt wird.|

