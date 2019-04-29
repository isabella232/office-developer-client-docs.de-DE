---
title: Unterstützung für formatierte Text Gateway-zuStändigkeiten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d5c3480018be399a85ee0bfda7ce1ff9b701cecc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419429"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>Unterstützung von formatiertem Text: Aufgaben des Gateways

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So behandeln Sie Rich-Text-Formate für ausgehende Nachrichten, Gateways**
  
1. Ruft nur die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft einer Nachricht aus dem Nachrichtenspeicher ab. Der Hauptvorteil beim Abrufen der **PR_RTF_COMPRESSED** -Eigenschaft besteht darin, dass der Nachrichtentext nicht zwischen Computern gesendet werden muss, wenn das Gateway und der Nachrichtenspeicher auf unterschiedlichen Computern vorhanden sind. 
    
2. Generieren Sie den Nachrichtentext aus dem formatierten Text, indem Sie die RTF-Bibliotheksfunktion **HrTextFromCompressedRTFStream** aufrufen oder, falls die Nachricht lokal gespeichert ist, **RTFSync**. Das RTF_SYNC_RTF_CHANGED-Flag sollte im Aufruf von **RTFSync**festgelegt werden. Weitere Informationen finden Sie unter [RTFSync](rtfsync.md).
    
3. Nehmen Sie irreversible Änderungen am Nachrichtentext vor, beispielsweise nicht unterstützte Zeichen. 
    
4. Stellen Sie sicher, dass sowohl **PR_RTF_IN_SYNC** ([pidtagrtfinsync (](pidtagrtfinsync-canonical-property.md)) als auch alle RTF-Hilfsbetriebe-Eigenschaften entweder festgelegt oder abwesend sind.
    
5. Wenn Änderungen vorgenommen wurden, rufen Sie **RTFSync** mit den RTF_SYNC_RTF_CHANGED-und RTF_SYNC_BODY_CHANGED-Flags auf. **RTFSync** berechnet die RTF-Hilfsbetriebe-Eigenschaften aus dem geänderten Text neu. 
    
6. Nehmen Sie beliebige Änderungen am Nachrichtentext vor, beispielsweise Einfügen von Anlagen Platzhaltern und Durchführen von nicht zerstörerischen Codepage-Konvertierungen.
    
7. Senden Sie die Nachricht.
    
 **So behandeln Sie Rich-Text-Formate für eingehende Nachrichten, Gateways**
  
1. Rückgängige Nachrichtentext Änderungen, die direkt vor dem Senden der Nachricht vorgenommen wurden. 
    
2. Rufen Sie **RTFSync** auf, wenn die Nachricht sowohl die **PR_RTF_COMPRESSED** -als auch die **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft enthält. 
    
3. Aktualisieren Sie die Nachricht im Nachrichtenspeicher mit der **PR_RTF_COMPRESSED** -Eigenschaft, wenn Sie von der Nachricht enthalten ist. Aktualisieren Sie nur mit der **PR_BODY** -Eigenschaft, wenn **PR_RTF_COMPRESSED** fehlt. 
    
4. VerWerfen Sie **PR_BODY** , wenn die Nachricht sowohl diese Eigenschaft als auch **PR_RTF_COMPRESSED**enthält.
    
Gateways rufen **RTFSync** auf, um zu vermeiden, dass sowohl der Nachrichtentext als auch der formatierte Text übertragen werden, wenn sich der Nachrichtenspeicher auf einem anderen Computer befindet. Wenn das Gateway lokal ist, kann es beide Eigenschaften festlegen und dem Nachrichtenspeicher die Ausführung der Synchronisierung gestatten. 
  

