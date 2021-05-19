---
title: Unterstützen von Verantwortlichkeiten für formatierte Textgateways
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
# <a name="supporting-formatted-text-gateway-responsibilities"></a>Unterstützen von formatierten Text: Gateway-Verantwortlichkeiten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **To handle Rich Text Format for outgoing messages, gateways**
  
1. Rufen Sie nur die eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) einer Nachricht aus dem Nachrichtenspeicher ab. Der Hauptvorteil beim Abrufen nur der **PR_RTF_COMPRESSED-Eigenschaft** ist, dass der Nachrichtentext nicht zwischen Computern gesendet werden muss, wenn das Gateway und der Nachrichtenspeicher auf verschiedenen Computern vorhanden sind. 
    
2. Generieren Sie den Nachrichtentext aus dem formatierten Text entweder durch Aufrufen der RTF-Bibliotheksfunktion **HrTextFromCompressedRTFStream** oder, wenn die Nachricht lokal gespeichert wird, **RTFSync**. Das RTF_SYNC_RTF_CHANGED sollte im Aufruf von **RTFSync festgelegt werden.** Weitere Informationen finden Sie unter [RTFSync](rtfsync.md).
    
3. Nehmen Sie unwiderrufliche Änderungen am Nachrichtentext vor, z. B. das Ablegen nicht unterstützter Zeichen. 
    
4. Stellen Sie **sicher, PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) und alle #A0 entweder festgelegt oder nicht vorhanden sind.
    
5. Wenn Änderungen vorgenommen wurden, rufen Sie **RTFSync** auf, RTF_SYNC_RTF_CHANGED und RTF_SYNC_BODY_CHANGED festgelegt sind. **RTFSync** berechnet die rtF-Hilfseigenschaften aus dem geänderten Text neu. 
    
6. Nehmen Sie umkehrbare Änderungen am Nachrichtentext vor, z. B. das Einfügen von Anlagenplatzhaltern und das Ausführen von nicht destruktiven Codeseitenkonvertierungen.
    
7. Senden Sie die Nachricht.
    
 **To handle Rich Text Format for incoming messages, gateways**
  
1. Rückgängig machen sie alle Änderungen am Nachrichtentext, die direkt vor dem Senden der Nachricht vorgenommen wurden. 
    
2. Rufen **Sie RTFSync** auf, wenn die Nachricht die Eigenschaften **PR_RTF_COMPRESSED** und **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) enthält. 
    
3. Aktualisieren Sie die Nachricht im Nachrichtenspeicher mit **der PR_RTF_COMPRESSED-Eigenschaft,** wenn die Nachricht sie enthält. nur dann mit **der PR_BODY-Eigenschaft** **aktualisieren, PR_RTF_COMPRESSED** nicht vorhanden ist. 
    
4. Verwerfen **PR_BODY,** wenn die Nachricht sowohl diese Eigenschaft als auch **PR_RTF_COMPRESSED.**
    
Gateways rufen **RTFSync auf,** um die Übertragung des Nachrichtentexts und des formatierten Texts zu vermeiden, wenn sich der Nachrichtenspeicher auf einem anderen Computer befindet. Wenn das Gateway lokal ist, kann es beide Eigenschaften festlegen und dem Nachrichtenspeicher erlauben, die Synchronisierung durchzuführen. 
  

