---
title: TNEF-Korrelation in SMTP-Gateways und-Übertragungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0a685e081d319c43daa583d95d163677e81f2480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413668"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>TNEF-Korrelation in SMTP-Gateways und-Übertragungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gateways und Übertragungen, die eine Verbindung mit internetbasierten Systemen herstellen, die SMTP verwenden, verwenden Sie den Wert des SMTP-Headers MessageID und die **PR_TNEF_CORRELATION_KEY** -Eigenschaft, um die TNEF-Korrelation zu implementieren. 
  
Der Wert der MessageID-Kopfzeile der ausgehenden Nachricht sollte in die **PR_TNEF_CORRELATION_KEY** ([pidtagtnefcorrelationkey (](pidtagtnefcorrelationkey-canonical-property.md))-Eigenschaft kopiert und im [attMAPIProps](attmapiprops.md) -Attribut des TNEF-Streams codiert werden. Beachten Sie, dass **PR_TNEF_CORRELATION_KEY** eine binäre Eigenschaft ist, während die MessageId eine Zeichenfolge ist; das NULL-Terminator sollte in der Kopie und im Vergleich enthalten sein. 
  
Diese Technik wird von allen Microsoft-Software verwendet, die MAPI-basierte Messagingsysteme mit dem Internet verbindet, wie beispielsweise Microsoft Exchange Server. Diese Technik sollte von allen SMTP-Gateways und-Übertragungen verwendet werden, die eine Verbindung zu Systemen herstellen, die MAPI-Clients unterstützen, um die Interoperabilität zu maximieren.
  

