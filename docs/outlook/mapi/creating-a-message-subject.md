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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332963"
---
# <a name="creating-a-message-subject"></a>Erstellen eines Nachrichtenbetreffs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Betreff einer Nachricht, **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md)), ist eine optionale Eigenschaft, mit der der Zweck einer Nachricht zusammengefasst wird. Wenn Sie festlegen, dass es sich um eine Zeichenfolge von 128 Byte oder niedriger. Das 128-Byte-Limit ist kein Grenzwert, der von MAPI auferlegt wird. Es handelt sich um eine Grenze, die von einigen Nachrichtenspeicher Anbietern auferlegt wird. Um die Interoperabilität mit Anbietern zu gewährleisten, die dies erzwingen, begrenzen Sie die Anzahl der Probanden auf 128 Byte. 
  
Beachten Sie, dass einige Nachrichtenspeicher Anbieter nicht zulassen, dass **PR_Subject** in einen Stream mit der [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Schnittstelle geschrieben wird. 
  
Legen Sie **PR_SUBJECT_PREFIX** ([pidtagsubjectprefix (](pidtagsubjectprefix-canonical-property.md)) nicht fest. Diese Eigenschaft wird nur für Antworten und weitergeleitete Nachrichten festgelegt. 
  

