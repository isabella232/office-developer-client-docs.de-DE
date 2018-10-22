---
title: InternetTimeout-Eigenschaft (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd0fdc8f64207e1233ac56812ef009da865ce01a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603462"
---
# <a name="internettimeout-property-rds"></a>InternetTimeout-Eigenschaft (RDS)


**Betrifft**: Access 2013 | Office 2013

Gibt an, wie viele Millisekunden bis zum Erreichen des Timeouts einer Anforderung gewartet wird.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Legt einen **Long** -Wert fest, der die Anzahl von Millisekunden vor dem Timeout der Anforderung darstellt, oder gibt den Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gilt nur für Anforderungen, die mit den Protokollen HTTP oder HTTPS gesendet werden.

In einer dreistufigen Umgebung kann es mehrere Minuten dauern, bis eine Anforderung ausgeführt wird. Geben Sie mit dieser Eigenschaft zusätzliche Zeit für länger dauernde Anforderungen an.
