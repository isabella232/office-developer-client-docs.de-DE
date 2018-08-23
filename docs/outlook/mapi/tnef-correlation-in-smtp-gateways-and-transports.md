---
title: TNEF-Korrelation in SMTP-Gateways und Transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8192646007e8935a750a70e46b8210eebbc353f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578535"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>TNEF-Korrelation in SMTP-Gateways und Transport

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gateways und Transport, die mit dem Internet verbunden-basierte Systeme, mit denen SMTP verwenden, verwenden Sie den Wert von MessageID SMTP-Kopfzeile und die **PR_TNEF_CORRELATION_KEY** -Eigenschaft zur Implementierung einer TNEF Korrelation. 
  
Der Wert der MessageID-Header der ausgehende Nachricht sollte der **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))-Eigenschaft kopiert und in das [AttMAPIProps](attmapiprops.md) -Attribut des Datenstroms TNEF codiert werden. Beachten Sie, dass **PR_TNEF_CORRELATION_KEY** eine binäre Eigenschaft, die MessageID eine Zeichenfolge ist. die null-Terminator sollte in der Kopie und im Vergleich eingefügt werden. 
  
Dieses Verfahren wird von allen Microsoft-Software verwendet, die mit dem Internet, wie beispielsweise Microsoft Exchange Server MAPI-basierten Messagingsystemen verbindet. Dieses Verfahren sollte verwendet werden, durch eine beliebige SMTP-Gateways und Transport, die mit Systemen, die MAPI-Clients unterstützen verbunden, um die Interoperabilität zu maximieren.
  

