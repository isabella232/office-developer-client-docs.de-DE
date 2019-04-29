---
title: Transport-Neutral Encapsulation Format (TNEF)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: 'Letzte Änderung: 12. März 2013'
ms.openlocfilehash: d902039fa1081e30947ddd8f70ead9ae7acec06a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428690"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a>Transport-Neutral Encapsulation Format (TNEF)

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
TNEF ist ein Format zur Konvertierung einer Reihe von MAPI-Eigenschaften – einer MAPI-Nachricht – in einen seriellen Datenstrom. Die TNEF-Funktionen werden in erster Linie von Transportanbietern verwendet, die MAPI-Nachrichteneigenschaften für die Übertragung über ein Messagingsystem codieren müssen, das diese Eigenschaften nicht direkt unterstützt. Beispielsweise verwendet ein SMTP-basierter Transport TNEF zum Codieren von Eigenschaften wie **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), die keine direkten Darstellungen in der Struktur einer SMTP-Nachricht aufweisen.
  
Die TNEF-Implementierung definiert mehrere TNEF-spezifische Attribute, die jeweils einer bestimmten MAPI-Eigenschaft entsprechen. Diese Attribute werden verwendet, um ihre jeweiligen MAPI-Eigenschaften in den TNEF-Stream zu codieren. Darüber hinaus wird ein spezielles Attribut definiert, mit dem alle MAPI-Eigenschaften gekapselt werden können, die nicht über ein bestimmtes Attribut entsprechen. Der Grund dafür, dass diese Attribute definiert werden, besteht darin, statt einfach eine einheitliche Codierungsmethode für alle MAPI-Eigenschaften zu verwenden, die Abwärtskompatibilität mit nicht-MAPI-kompatiblen Software zu aktivieren, die TNEF verwendet.
  
Im restlichen Teil dieses Abschnitts werden die Struktur und Syntax eines TNEF-Streams, die Zuordnung zwischen MAPI-Eigenschaften und TNEF-Attributen sowie wichtige Überlegungen zu bestimmten TNEF-Attributen beschrieben.
  

