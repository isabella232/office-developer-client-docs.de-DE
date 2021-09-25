---
title: Transport-Neutral Encapsulation Format (TNEF)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: 'Letzte Änderung: 12. März 2013'
ms.openlocfilehash: 22ba19f374421656317196080e6a22153700f851
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590909"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a>Transport-Neutral Encapsulation Format (TNEF)

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
TNEF ist ein Format zur Konvertierung einer Reihe von MAPI-Eigenschaften – einer MAPI-Nachricht – in einen seriellen Datenstrom. Die TNEF-Funktionen werden in erster Linie von Transportanbietern verwendet, die MAPI-Nachrichteneigenschaften für die Übertragung über ein Messagingsystem codieren müssen, das diese Eigenschaften nicht direkt unterstützt. Beispielsweise verwendet ein SMTP-basierter Transport TNEF zum Codieren von Eigenschaften wie **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), die keine direkten Darstellungen in der Struktur einer SMTP-Nachricht haben.
  
Die TNEF-Implementierung definiert mehrere TNEF-spezifische Attribute, die jeweils einer bestimmten MAPI-Eigenschaft entsprechen. Diese Attribute werden verwendet, um ihre jeweiligen MAPI-Eigenschaften im TNEF-Stream zu codieren. Darüber hinaus wird ein spezielles Attribut definiert, das verwendet werden kann, um jede MAPI-Eigenschaft zu kapseln, die nicht über ein bestimmtes Attribut verfügt, das ihr entspricht. Der Grund dafür, warum diese Attribute definiert werden, ist nicht nur die Verwendung einer einheitlichen Codierungsmethode für alle MAPI-Eigenschaften, sondern die Aktivierung der Abwärtskompatibilität mit nicht MAPI-kompatibler Software, die TNEF verwendet.
  
Im restlichen Teil dieses Abschnitts werden die Struktur und Syntax eines TNEF-Datenstroms, die Zuordnung zwischen MAPI-Eigenschaften und TNEF-Attributen sowie wichtige Überlegungen für bestimmte TNEF-Attribute beschrieben.
  

