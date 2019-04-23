---
title: OnError-Ereignis (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288476"
---
# <a name="onerror-event-rds"></a>OnError-Ereignis (RDS)

**Gilt für**: Access 2013, Office 2013

Wenn während eines Vorgangs ein Fehler auftritt, wird das **OnError**-Ereignis aufgerufen.

## <a name="syntax"></a>Syntax

OnError*SCode*, *Description*, *Source*, *CancelDisplay as*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*SCode* |Eine ganze Zahl, die den Statuscode des Fehlers angibt.|
|*Description* |A **String** that indicates a description of the error.|
|*Quelle* |A **String** that indicates the query or command that caused the error.|
|*CancelDisplay as* |A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.|

