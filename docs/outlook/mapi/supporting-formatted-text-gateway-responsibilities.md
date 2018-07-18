---
title: Unterstützung von formatierten Text Gateway Zuständigkeiten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6d2c85aa76a372ba79e55dbf5b22024288214df6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795663"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>Unterstützung von formatiertem Text: Aufgaben des Gateways

  
  
**Betrifft**: Outlook 
  
 **Zum Verarbeiten von Rich-Text-Format für ausgehende Nachrichten, gateways**
  
1. Rufen Sie nur eine Nachricht **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft aus dem Nachrichtenspeicher ab. Der Hauptvorteil Abrufen nur die **PR_RTF_COMPRESSED** -Eigenschaft ist, dass der Nachrichtentext nicht zwischen Computern gesendet werden, wenn das Gateway und dem Nachrichtenspeicher auf verschiedenen Computern vorhanden sein muss. 
    
2. Generieren Sie dem Nachrichtentext aus der formatierte Text entweder durch den Aufruf von RTF-Library-Funktion **HrTextFromCompressedRTFStream** oder, falls die Nachricht lokal gespeichert ist **RTFSync**. Das Flag RTF_SYNC_RTF_CHANGED sollte in den Aufruf von **RTFSync**festgelegt werden. Weitere Informationen finden Sie unter [RTFSync](rtfsync.md).
    
3. Stellen Sie den Nachrichtentext, z. B. das Verwerfen nicht unterstützter Zeichen in irgendeiner Weise nicht rückgängig gemacht werden. 
    
4. Stellen Sie sicher, dass **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) und alle RTF Auxilliary Eigenschaften entweder festgelegt sind oder nicht vorhanden.
    
5. Wenn alle Änderungen vorgenommen wurden, rufen Sie mit der RTF_SYNC_RTF_CHANGED und die RTF_SYNC_BODY_CHANGED Flags **RTFSync** . **RTFSync** wird die RTF Auxilliary Eigenschaften aus dem geänderten Text neu berechnen. 
    
6. Stellen Sie alle umkehrbar Änderungen an den Nachrichtentext, wie Anlagen Platzhalter einfügen und nicht zerstörerische Codepages ausführen.
    
7. Senden der Nachricht.
    
 **Zum Verarbeiten von Rich-Text-Format für eingehende Nachrichten gateways**
  
1. Umgekehrte Modifikationen Text Nachricht, die direkt vorgenommen wurden, bevor die Nachricht gesendet wurde. 
    
2. Rufen Sie **RTFSync** , wenn die Nachricht die **PR_RTF_COMPRESSED** und die Eigenschaften **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) enthält. 
    
3. Aktualisieren Sie die Nachricht im Nachrichtenspeicher mit der **PR_RTF_COMPRESSED** -Eigenschaft, wenn die Meldung Es enthält; Aktualisieren Sie mit der **PR_BODY** -Eigenschaft nur, wenn **PR_RTF_COMPRESSED** nicht vorhanden ist. 
    
4. Verwerfen Sie **PR_BODY** , wenn die Nachricht diese Eigenschaft und die **PR_RTF_COMPRESSED**enthält.
    
Gateways Aufrufen **RTFSync** zur Vermeidung der Nachrichtentext und die formatierten Text übertragen, wenn der Nachrichtenspeicher auf einem anderen Computer ist. Wenn das Gateway lokal ist, kann die Eigenschaften festgelegt werden und des Nachrichtenspeichers für die Synchronisierung zulassen. 
  

