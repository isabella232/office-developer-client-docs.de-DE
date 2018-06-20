---
title: Kanonische PidTagMappingSignature-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0a83e0aa8f7ab1eb1f30e3ba97d3ea36f16fd873
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794581"
---
# <a name="pidtagmappingsignature-canonical-property"></a>Kanonische PidTagMappingSignature-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Die Zuordnung Signatur für benannte Eigenschaften eines bestimmten MAPI-Objekts enthält. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_MAPPING_SIGNATURE  <br/> |
|Bezeichner:  <br/> |0x0FF8  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Verschiedenes  <br/> |
   
## <a name="remarks"></a>Hinweise

Es wird empfohlen, diese Eigenschaft für Objekte mit dem benannten Eigenschaften verfügbar machen. Eine Clientanwendung sollte überprüfen Sie die Eigenschaft **PR_MAPPING_SIGNATURE** beider übergebener Objekte beim Kopieren mit dem Eigenschaften eines Objekts in einen anderen Namen. Verwendung dieser Eigenschaft können Sie minimieren übersetzen zwischen Namen und Bezeichner kopierten Eigenschaften. 
  
Wenn diese Eigenschaft für ein bestimmtes MAPI-Objekt nicht vorhanden ist, hat das Objekt eine eigene eindeutige Zuordnung von Namen und Bezeichner. In diesem Fall muss der Client die [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) -Methode für das Quellobjekt und dann die [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode für das Zielobjekt aufrufen. 
  
Wenn zwei Objekte den gleichen Wert **PR_MAPPING_SIGNATURE** sind, muss der Client nicht Name, ID und Name-ID übersetzen. Der Client kann die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode auf das Ziel einfach auf die Quelle, und klicken Sie dann die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode aufrufen. Dies ist hilfreich für Clients, die benutzerdefinierte Kopieren von benannten Eigenschaften ausführen, und der Anbieter die [IMAPIProp::CopyTo](imapiprop-copyto.md) und [IMAPIProp::CopyProps](imapiprop-copyprops.md) -Methoden implementieren. 
  
Weitere Informationen zu benannten Eigenschaften und Zuordnung von Namen und Bezeichner finden Sie unter [MAPI-Eigenschaften mit dem Namen](mapi-named-properties.md). 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPINAMEID](mapinameid.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

