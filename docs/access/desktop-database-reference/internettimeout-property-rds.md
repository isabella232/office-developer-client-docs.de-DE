---
title: InternetTimeout-Eigenschaft (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fb247396b5e7e65c9fbfe86ab4f06b6a69037522
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631937"
---
# <a name="internettimeout-property-rds"></a>InternetTimeout-Eigenschaft (RDS)


**Gilt für**: Access 2013, Office 2013

Gibt an, wie viele Millisekunden bis zum Erreichen des Timeouts einer Anforderung gewartet wird.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Legt einen **Long**-Wert fest, der die Anzahl von Millisekunden vor dem Timeout der Anforderung darstellt, oder gibt den Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gilt nur für Anforderungen, die mit den Protokollen HTTP oder HTTPS gesendet werden.

In einer dreistufigen Umgebung kann es mehrere Minuten dauern, bis eine Anforderung ausgeführt wird. Geben Sie mit dieser Eigenschaft zusätzliche Zeit für länger dauernde Anforderungen an.

