---
title: Kanonische PidLidEmail2OriginalDisplayName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3e3c71d8eafb077e70535bd8515521eb0734556b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566969"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a>Kanonische PidLidEmail2OriginalDisplayName-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den zweiten Anzeigenamen an, der der für den Kontakt angegebenen E-Mail-Adresse entspricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidEmail2OriginalDisplayName  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008094  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der Wert der **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) -Eigenschaft "SMTP" ist, sollte der Wert der entsprechenden **PidLidEmail2OriginalDisplayName** -Eigenschaft dem Wert der entsprechenden **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) -Eigenschaft entsprechen. Der Zweck dieser Eigenschaft besteht darin, eine alternative benutzerfreundliche Adresse anzuzeigen, die der Adresse in der **dispidEmail2EmailAddress** entspricht.
  
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

