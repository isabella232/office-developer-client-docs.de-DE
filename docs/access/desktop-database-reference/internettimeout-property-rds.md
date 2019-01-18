---
title: InternetTimeout-Eigenschaft (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0650a287e2aebc13b89572db112b8f9b333dc6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710076"
---
# <a name="internettimeout-property-rds"></a>InternetTimeout-Eigenschaft (RDS)


**Betrifft**: Access 2013, Office 2013

Gibt an, wie viele Millisekunden bis zum Erreichen des Timeouts einer Anforderung gewartet wird.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Long** -Wert fest, der die Anzahl von Millisekunden vor dem Timeout der Anforderung darstellt, oder gibt den Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gilt nur für Anforderungen, die mit den Protokollen HTTP oder HTTPS gesendet werden.

In einer dreistufigen Umgebung kann es mehrere Minuten dauern, bis eine Anforderung ausgeführt wird. Geben Sie mit dieser Eigenschaft zusätzliche Zeit für länger dauernde Anforderungen an.

