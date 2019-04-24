---
title: Kanonische Pidlidusetnef (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 56f6e2355ee2e64cc766bafe27cd59454e210ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315421"
---
# <a name="pidlidusetnef-canonical-property"></a>Kanonische Pidlidusetnef (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob TNEF (Transport Neutral Encapsulation Format) in eine Nachricht eingeschlossen werden soll, wenn diese Nachricht von MAPI zu Multipurpose Internet Mail Extensions (MIME) oder SMTP-Format (Simple Mail Transfer Protocol) konvertiert wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidUseTNEF  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long-ID (Deckel):  <br/> |0x00008582  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Laufzeitkonfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt an, ob TNEF in eine Nachricht eingeschlossen werden soll, wenn diese Nachricht von TNEF in MIME oder SMTP-Format konvertiert wird. Diese Eigenschaft ist möglicherweise abwesend, und wenn dies der Fall ist, muss TNEF in der Nachricht nicht enthalten sein.
  
Diese Eigenschaft gilt nur, wenn die Nachricht von einem POP3/SMTP-e-Mail-Konto gesendet wird und nicht angewendet wird, wenn die Nachricht von anderen Anbietern wie Microsoft Exchange Server gesendet wird.
  
Unter bestimmten Umständen, beispielsweise bei der Aktivierung von Abstimmungsschaltflächen oder einem eingebetteten OLE-Objekt an eine Nachricht, kann Outlook diese Eigenschaft festlegen, um die Verwendung von TNEF zu erzwingen.
  
Die **PR_MSG_EDITOR_FORMAT** ([pidtagmessageeditorformat (](pidtagmessageeditorformat-canonical-property.md))-Eigenschaft kann verwendet werden, um beim Senden einer Nachricht nur einfachen Text und nicht TNEF zu erzwingen. Da **pidlidusetnef (** die Einstellung in **PR_MSG_EDITOR_FORMAT**überschreibt, sollte eine Anwendung, die nur Text in einer ausgehenden Nachricht erzwingen möchte, auch nach **PIDLIDUSETNEF (** suchen und Sie auf false zurücksetzen. Darüber hinaus muss das Add-in die Nachrichten Features entfernen, die TNEF benötigt haben, um unbrauchbare Anlagen für die Nachricht zu vermeiden, die schließlich gesendet wird. 
  
Verwenden Sie das **CCSF_USE_TNEF** -Flag beim Aufrufen von [IConverterSession:: MAPItoMIMEStm](iconvertersession-mapitomimestm.md) zum Konvertieren einer ausgehenden MAPI-Nachricht in einen MIME-Stream kann auch TNEF erzwungen werden. Dies gilt auch dann, wenn **pidlidusetnef (** nicht festgelegt ist. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

