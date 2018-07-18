---
title: PidLidEmail1OriginalDisplayName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail1OriginalDisplayName
api_type:
- COM
ms.assetid: 991c2969-0180-4c7d-95ee-e62fd24d67ef
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7d09830f471fbaa0e8ed6ae70420dfea6428b9df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793513"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a>PidLidEmail1OriginalDisplayName (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt den ersten Anzeigenamen, der die die e-Mail-Adresse entspricht, die für den Kontakt angegeben ist.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidEmail1OriginalDisplayName  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Address  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008084  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn der Wert der Eigenschaft **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) "SMTP" ist, sollte der Wert der jeweiligen **dispidEmail1OriginalDisplayName** -Eigenschaft den Wert der jeweiligen **entsprechen. dispidEmail1EmailAddress** -Eigenschaft ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)). Diese Eigenschaft zeigt eine alternative benutzerfreundliche Adresse, die in der **dispidEmail1EmailAddress** -Eigenschaft entspricht. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

