---
title: onError-Ereignis (RDS)
TOCTitle: onError Event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3fe6f6b78297008e25e15dc17e243ae982a5ccf3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475768"
---
# <a name="onerror-event-rds"></a>onError-Ereignis (RDS)


**Betrifft**: Access 2013 | Office 2013

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

