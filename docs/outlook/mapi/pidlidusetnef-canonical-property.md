---
title: Kanonische PidLidUseTnef-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d5d38f98402c0804633d3bcb0f9ca196fa15795f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610055"
---
# <a name="pidlidusetnef-canonical-property"></a>Kanonische PidLidUseTnef-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob das transportneutrale Kapselungsformat (Transport Neutral Encapsulation Format, TNEF) in eine Nachricht eingeschlossen werden soll, wenn diese Nachricht von mapi in MIME (Multipurpose Internet Mail Extensions) oder smtp-Format (Simple Mail Transfer Protocol) konvertiert wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidUseTNEF  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008582  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Laufzeitkonfiguration  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft gibt an, ob TNEF in eine Nachricht eingeschlossen werden soll, wenn diese Nachricht vom TNEF-Format in das MIME- oder SMTP-Format konvertiert wird. Diese Eigenschaft ist möglicherweise nicht vorhanden, und wenn ja, darf TNEF nicht in der Nachricht enthalten sein.
  
Diese Eigenschaft gilt nur, wenn die Nachricht von einem POP3/SMTP-E-Mail-Konto gesendet wird, und nicht, wenn die Nachricht von anderen Anbietern wie Microsoft Exchange Server gesendet wird.
  
Unter bestimmten Umständen, z. B. wenn Abstimmungsschaltflächen aktiviert sind oder ein eingebettetes OLE-Objekt an eine Nachricht angefügt ist, können Outlook diese Eigenschaft festlegen, um die Verwendung von TNEF zu erzwingen.
  
Die **eigenschaft PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) kann verwendet werden, um beim Senden einer Nachricht nur Nur-Text und nicht TNEF zu erzwingen. Da **PidLidUseTNEF** die Einstellung in **PR_MSG_EDITOR_FORMAT** überschreibt, sollte eine Anwendung, die Nur-Text für eine ausgehende Nachricht erzwingen möchte, auch nach **PidLidUseTNEF** suchen und auf FALSE zurücksetzen. Darüber hinaus muss das Add-In die Nachrichtenfeatures entfernen, die TNEF erforderten, um nicht verwendbare Anlagen der Nachricht zu vermeiden, die schließlich gesendet wird. 
  
Verwenden Sie das **CCSF_USE_TNEF** Flag beim Aufrufen von [IConverterSession::MAPIToMIMEStm,](iconvertersession-mapitomimestm.md) um eine ausgehende MAPI-Nachricht in einen MIME-Stream zu konvertieren, kann auch TNEF erzwingen. Dies gilt auch, wenn **PidLidUseTNEF** nicht festgelegt ist. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Anlagenobjekte in einer effizienten Datenstromdarstellung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

