---
title: Erstellen eines Nachrichtenbetreffs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b5ae0c8e16af35b730d6a1fbdcf95b74c6119e1b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631072"
---
# <a name="creating-a-message-subject"></a>Erstellen eines Nachrichtenbetreffs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Betreff einer Nachricht, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), ist eine optionale Eigenschaft, die verwendet wird, um die Absicht einer Nachricht zusammenzufassen. Wenn Sie die Zeichenfolge festlegen möchten, legen Sie sie als Zeichenfolge mit einer Größe von 128 Byte oder weniger fest. Der Grenzwert von 128 Byte ist kein grenzwert, der von der MAPI festgelegt wird. Es handelt sich um einen Grenzwert, der von einigen Nachrichtenspeicheranbietern festgelegt wird. Um die Interoperabilität mit Anbietern sicherzustellen, die dies auferlegen, beschränken Sie die Betreffdaten auf 128 Bytes. 
  
Beachten Sie, dass einige Nachrichtenspeicheranbieter nicht zulassen, **dass PR_SUBJECT** mit der [IStream-Schnittstelle](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) in einen Datenstrom geschrieben werden. 
  
**PR_SUBJECT_PREFIX** nicht festlegen ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Diese Eigenschaft wird nur für Antworten und weitergeleitete Nachrichten festgelegt. 
  

