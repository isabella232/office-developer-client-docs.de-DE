---
title: onError-Ereignis (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 49a9f5340ac12218ef2c1a85e9930566a147a3fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626260"
---
# <a name="onerror-event-rds"></a>onError-Ereignis (RDS)

**Gilt für**: Access 2013, Office 2013

Wenn während eines Vorgangs ein Fehler auftritt, wird das **OnError**-Ereignis aufgerufen.

## <a name="syntax"></a>Syntax

onError *SCode*, *Description*, *Source*, *CancelDisplay*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*SCode* |Eine ganze Zahl, die den Statuscode des Fehlers angibt.|
|*Description* |A **String** that indicates a description of the error.|
|*Quelle* |A **String** that indicates the query or command that caused the error.|
|*CancelDisplay* |A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.|

