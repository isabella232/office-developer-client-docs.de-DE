---
title: Unterstützung formatierter Textgatewayaufgaben
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fe73b2ea48faa3064bee839aa997ff2d0875716c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629550"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>Unterstützen von formatiertem Text: Gateway-Zuständigkeiten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So behandeln Sie rich-Text-Format für ausgehende Nachrichten, Gateways**
  
1. Ruft nur die **PR_RTF_COMPRESSED** -[PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) -Eigenschaft einer Nachricht aus dem Nachrichtenspeicher ab. Der Hauptvorteil beim Abrufen nur der **PR_RTF_COMPRESSED-Eigenschaft** besteht darin, dass der Nachrichtentext nicht zwischen Computern gesendet werden muss, wenn das Gateway und der Nachrichtenspeicher auf verschiedenen Computern vorhanden sind. 
    
2. Generieren Sie den Nachrichtentext aus dem formatierten Text, indem Sie entweder die RTF-Bibliotheksfunktion **HrTextFromCompressedRTFStream** aufrufen oder, wenn die Nachricht lokal gespeichert wird, **RTFSync**. Das RTF_SYNC_RTF_CHANGED Flag sollte im Aufruf von **RTFSync** festgelegt werden. Weitere Informationen finden Sie unter [RTFSync](rtfsync.md).
    
3. Nehmen Sie alle unumkehrbaren Änderungen am Nachrichtentext vor, z. B. das Ablegen nicht unterstützter Zeichen. 
    
4. Stellen Sie sicher, dass **sowohl PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) als auch alle RTF-auxilliary-Eigenschaften festgelegt oder nicht vorhanden sind.
    
5. Wenn Änderungen vorgenommen wurden, rufen Sie **RTFSync** auf, wobei sowohl die RTF_SYNC_RTF_CHANGED als auch RTF_SYNC_BODY_CHANGED Flags festgelegt sind. **RTFSync** berechnet die RTF-Hilfseigenschaften aus dem geänderten Text neu. 
    
6. Nehmen Sie alle umkehrbaren Änderungen am Nachrichtentext vor, z. B. das Einfügen von Anlagenplatzhaltern und das Ausführen nicht destruktiver Codepagekonvertierungen.
    
7. Senden Sie die Nachricht.
    
 **So behandeln Sie rich-Text-Format für eingehende Nachrichten, Gateways**
  
1. Alle Nachrichtentextänderungen rückgängig machen, die direkt vor dem Senden der Nachricht vorgenommen wurden. 
    
2. Rufen Sie **RTFSync** auf, wenn die Nachricht die Eigenschaften **PR_RTF_COMPRESSED** und **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) enthält. 
    
3. Aktualisieren Sie die Nachricht im  Nachrichtenspeicher mit der PR_RTF_COMPRESSED-Eigenschaft, wenn die Nachricht sie enthält. mit der **PR_BODY-Eigenschaft** nur aktualisieren, wenn **PR_RTF_COMPRESSED** nicht vorhanden ist. 
    
4. Verwerfen Sie **PR_BODY,** wenn die Nachricht sowohl diese Eigenschaft als **auch PR_RTF_COMPRESSED** enthält.
    
Gateways rufen **RTFSync** auf, um zu vermeiden, dass nachrichtentext und formatierter Text übertragen werden, wenn sich der Nachrichtenspeicher auf einem anderen Computer befindet. Wenn das Gateway lokal ist, kann es beide Eigenschaften festlegen und zulassen, dass der Nachrichtenspeicher die Synchronisierung durchführt. 
  

