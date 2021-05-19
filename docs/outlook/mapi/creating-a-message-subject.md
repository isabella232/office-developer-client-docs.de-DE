---
title: Erstellen eines Nachrichtensubjekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332963"
---
# <a name="creating-a-message-subject"></a>Erstellen eines Nachrichtensubjekts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Betreff einer Nachricht, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), ist eine optionale Eigenschaft, die verwendet wird, um die Absicht einer Nachricht zusammenzufassen. Wenn Sie sie festlegen möchten, müssen Sie eine Zeichenzeichenfolge von 128 Byte oder weniger festlegen. Der Grenzwert von 128 Byte ist kein von MAPI auferlegter Grenzwert. Es handelt sich um einen Grenzwert, der von einigen Nachrichtenspeicheranbietern auferlegt wird. Um die Interoperabilität mit Anbietern sicherzustellen, die dies durchsetzen, beschränken Sie die Anzahl der Betroffenen auf 128 Byte. 
  
Beachten Sie, dass einige Nachrichtenspeicheranbieter das Schreiben PR_SUBJECT in einen Datenstrom mit der [IStream-Schnittstelle nicht](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) zulassen.  
  
Legen Sie keine **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Diese Eigenschaft wird nur für Antworten und weitergeleitete Nachrichten festgelegt. 
  

