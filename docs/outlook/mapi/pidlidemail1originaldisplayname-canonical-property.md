---
title: Kanonische PidLidEmail1OriginalDisplayName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidEmail1OriginalDisplayName
api_type:
- COM
ms.assetid: 991c2969-0180-4c7d-95ee-e62fd24d67ef
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 577d1e4930899fb137b9b3a9df70580059af2e20
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587797"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a>Kanonische PidLidEmail1OriginalDisplayName-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den ersten Anzeigenamen an, der der E-Mail-Adresse entspricht, die für den Kontakt angegeben ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidEmail1OriginalDisplayName  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008084  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der Wert der **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) -Eigenschaft "SMTP" ist, sollte der Wert der entsprechenden **dispidEmail1OriginalDisplayName** -Eigenschaft dem Wert der entsprechenden **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) -Eigenschaft entsprechen. Diese Eigenschaft zeigt eine alternative benutzerfreundliche Adresse an, die der Adresse in der **dispidEmail1EmailAddress-Eigenschaft** entspricht. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

