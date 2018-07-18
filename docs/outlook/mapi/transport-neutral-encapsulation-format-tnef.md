---
title: Transport-Neutral Encapsulation Format (TNEF)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: 'Zuletzt geändert: 12 März 2013'
ms.openlocfilehash: 34b64df25cb2f7f591f7c799dec957a0072840dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795755"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a>Transport-Neutral Encapsulation Format (TNEF)

 
  
**Betrifft**: Outlook 
  
TNEF ist ein Format für die Konvertierung von einem Satz von MAPI-Eigenschaften – eine MAPI-Nachricht – in einen seriellen Datenstrom. Die TNEF-Funktionen werden in erster Linie von Anbietern Transport verwendet, die müssen MAPI-Eigenschaften für die Übertragung über einem messaging-System zu codieren, die diese Eigenschaften nicht direkt unterstützt. Beispielsweise verwendet ein SMTP-basierte Transport TNEF zum Codieren von Eigenschaften wie **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), die keine direkte Darstellungen in der Struktur einer SMTP-Nachricht besitzen.
  
Die TNEF-Implementierung definiert mehrere TNEF-spezifische Attribute, von die jedes eine bestimmte MAPI-Eigenschaft entspricht. Diese Attribute werden verwendet, um ihre jeweiligen MAPI-Eigenschaften in die TNEF-Stream codieren. Darüber hinaus ist ein spezielles Attribut definiert, die zum Kapseln von MAPI-Eigenschaften, die ein bestimmtes Attribut, es entspricht nicht verwendet werden können. Der Grund dafür, diese Attribute definiert werden – anstatt einfach eine einheitliche Codierungsverfahren für alle MAPI-Eigenschaften – Abwärtskompatibilität mit nicht-MAPI-kompatible Software zu aktivieren, die die TNEF verwendet wird.
  
Der Rest dieses Abschnitts wird die Struktur und Syntax von TNEF-Stream, der Zuordnung zwischen MAPI-Eigenschaften und TNEF-Attribute und wichtige Überlegungen für bestimmte TNEF-Attribute beschrieben.
  

