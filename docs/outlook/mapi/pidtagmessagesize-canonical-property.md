---
title: Kanonische PidTagMessageSize-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7da0e480af9761c1317c1941da1d68d448a1ef63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794619"
---
# <a name="pidtagmessagesize-canonical-property"></a>Kanonische PidTagMessageSize-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält die Summe der Größen aller Eigenschaften auf ein Meldungsobjekt in Bytes. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_MESSAGE_SIZE  <br/> |
|Bezeichner:  <br/> |0x0E08  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Es wird empfohlen, dass Message Objekte diese Eigenschaft verfügbar machen. Die Nachrichtengröße gibt die ungefähre Anzahl von Bytes, die übertragen werden, wenn die Nachricht von einem Informationsspeicher an eine andere verschoben wird. Wird die Summe der Größen aller Eigenschaften im Message-Objekt, ist es in der Regel deutlich größer als den Nachrichtentext allein. 
  
Die meisten Nachricht speichern Anbieter Compute diese Eigenschaft für Nachrichten, die sie behandeln. Einige Nachricht Anbieter unterstützt diese Eigenschaft jedoch nicht. Diese Eigenschaft ist in jedem Fall nicht verfügbar, bis die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) oder [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode aufgerufen wurde. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Ordner Vorgänge behandelt.
    
[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Gibt die zulässige Vorgänge für die Hauptobjekte der Nachricht Store.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

