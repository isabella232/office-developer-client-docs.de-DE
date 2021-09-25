---
title: TNEF-Korrelation in SMTP-Gateways und -Transporten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3cd51f3f48c236a17ee49f65368672ee849a5ed0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578480"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>TNEF-Korrelation in SMTP-Gateways und -Transporten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gateways und Transporte, die eine Verbindung mit internetbasierten Systemen herstellen, die SMTP verwenden, verwenden den Wert des SMTP-Headers MessageID und die **eigenschaft PR_TNEF_CORRELATION_KEY,** um die TNEF-Korrelation zu implementieren. 
  
Der Wert des MessageID-Headers der ausgehenden Nachricht sollte in die **eigenschaft PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) kopiert und im [attMAPIProps-Attribut](attmapiprops.md) des TNEF-Streams codiert werden. Beachten Sie, dass **PR_TNEF_CORRELATION_KEY** eine binäre Eigenschaft ist, während die MessageID eine Zeichenfolge ist. Der Null-Abschlusszeichen sollte in der Kopie und im Vergleich enthalten sein. 
  
Diese Technik wird von allen Microsoft-Software verwendet, die MAPI-basierte Messagingsysteme mit dem Internet verbindet, z. B. Microsoft Exchange Server. Diese Technik sollte von allen SMTP-Gateways und -Transporten verwendet werden, die eine Verbindung mit Systemen herstellen, die MAPI-Clients unterstützen, um die Interoperabilität zu maximieren.
  

