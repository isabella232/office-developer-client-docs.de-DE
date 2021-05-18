---
title: PidLidUseTnef (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 56f6e2355ee2e64cc766bafe27cd59454e210ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315421"
---
# <a name="pidlidusetnef-canonical-property"></a>PidLidUseTnef (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob das TNEF (Transport Neutral Encapsulation Format) in eine Nachricht eingeschlossen werden soll, wenn diese Nachricht von MAPI in mime (Multipurpose Internet Mail Extensions) oder SMTP (Simple Mail Transfer Protocol) konvertiert wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidUseTNEF  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Lange ID (LID):  <br/> |0x00008582  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Laufzeitkonfiguration  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt an, ob TNEF in eine Nachricht eingeschlossen werden soll, wenn diese Nachricht von TNEF in das MIME- oder SMTP-Format konvertiert wird. Diese Eigenschaft ist möglicherweise nicht vorhanden, und falls ja, darf TNEF nicht in die Nachricht eingeschlossen werden.
  
Diese Eigenschaft gilt nur, wenn die Nachricht von einem POP3/SMTP-E-Mail-Konto gesendet wird und nicht angewendet wird, wenn die Nachricht von anderen Anbietern gesendet wird, z. B. Microsoft Exchange Server.
  
Unter bestimmten Umständen, z. B. wenn Abstimmungsschaltflächen aktiviert sind oder ein eingebettetes OLE-Objekt an eine Nachricht angefügt ist, kann Outlook diese Eigenschaft so festlegen, dass die Verwendung von TNEF erzwingen wird.
  
Die **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) kann verwendet werden, um beim Senden einer Nachricht nur Nur-Text und nicht TNEF zu erzwingen. Da **PidLidUseTNEF** die Einstellung in **PR_MSG_EDITOR_FORMAT** außer Kraft setzt, sollte eine Anwendung, die Nur-Text für eine ausgehende Nachricht erzwingen möchte, auch **nach PidLidUseTNEF** suchen und auf FALSE zurücksetzen. Darüber hinaus muss das Add-In die Nachrichtenfeatures entfernen, für die TNEF erforderlich war, um unbrauchbare Anlagen für die Nachricht zu vermeiden, die schließlich gesendet wird. 
  
Verwenden Sie **das CCSF_USE_TNEF** beim Aufrufen von [IConverterSession::MAPIToMIMEStm,](iconvertersession-mapitomimestm.md) um eine ausgehende MAPI-Nachricht in einen MIME-Stream zu konvertieren, um auch TNEF zu erzwingen. Dies gilt auch dann, **wenn PidLidUseTNEF** nicht festgelegt ist. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

