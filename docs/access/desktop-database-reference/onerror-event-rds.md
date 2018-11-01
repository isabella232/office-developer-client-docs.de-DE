---
title: onError-Ereignis (RDS)
TOCTitle: onError Event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 17cbeece67ffa19666f6209a38159c9a2c6a44ea
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889945"
---
# <a name="onerror-event-rds"></a>onError-Ereignis (RDS)


**Betrifft**: Access 2013, Office 2013

Wenn während eines Vorgangs ein Fehler auftritt, wird das **OnError** -Ereignis aufgerufen.

## <a name="syntax"></a>Syntax

OnError*SCode*, *Beschreibung*, *Source*, *CancelDisplay*

## <a name="parameters"></a>Parameter

  - *SCode*

  - Eine ganze Zahl, die den Statuscode des Fehlers angibt.

  - *Description*

  - Eine **Zeichenfolge** , die eine Beschreibung des Fehlers angibt.

  - *Quelle*

  - Eine **Zeichenfolge** , die angibt, die Abfrage oder den Befehl, der den Fehler verursacht hat.

  - *CancelDisplay*

  - Ein **boolescher** Wert, die bei auf **True**festgelegt, die verhindert, dass den Fehler in einem Dialogfeld angezeigt wird.

