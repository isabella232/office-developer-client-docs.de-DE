---
title: Erstellen eines Nachrichtenbetreffs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395686"
---
# <a name="creating-a-message-subject"></a>Erstellen eines Nachrichtenbetreffs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Betreff der Nachricht **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) ist eine optionale-Eigenschaft verwendet, um den Zweck der eine Nachricht zusammenzufassen. Wenn diese Liste festgelegt werden soll, stellen Sie es eine Zeichenfolge 128 Byte oder weniger. Der 128 Byte-Grenzwert ist keiner-Limit MAPI. Es ist eine-Limit Zeichenfolgeneigenschaften einige Nachricht. Einschränken Sie, um die Interoperabilität mit Anbietern zu gewährleisten, die es bedingen Antragsteller 128 Byte. 
  
Beachten Sie, dass einige Anbieter Nachricht **PR_SUBJECT** in ein Stream-Objekt mit der [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Schnittstelle geschrieben werden nicht zulassen. 
  
Stellen Sie keine **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) Diese Eigenschaft ist nur für Antworten festlegen und weitergeleitete Nachrichten. 
  

