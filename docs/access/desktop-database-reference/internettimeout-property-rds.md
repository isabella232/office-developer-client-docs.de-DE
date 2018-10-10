---
title: InternetTimeout-Eigenschaft (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 929b166a308276836fbe4a48a2461ef7eb0caba2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472664"
---
# <a name="internettimeout-property-rds"></a>InternetTimeout-Eigenschaft (RDS)


**Betrifft**: Access 2013 | Office 2013

Gibt an, wie viele Millisekunden bis zum Erreichen des Timeouts einer Anforderung gewartet wird.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Long** -Wert fest, der die Anzahl von Millisekunden vor dem Timeout der Anforderung darstellt, oder gibt den Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gilt nur für Anforderungen, die mit den Protokollen HTTP oder HTTPS gesendet werden.

In einer dreistufigen Umgebung kann es mehrere Minuten dauern, bis eine Anforderung ausgeführt wird. Geben Sie mit dieser Eigenschaft zusätzliche Zeit für länger dauernde Anforderungen an.

