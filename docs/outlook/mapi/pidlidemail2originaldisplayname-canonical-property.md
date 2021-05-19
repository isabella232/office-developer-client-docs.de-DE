---
title: PidLidEmail2OriginalDisplayName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7fb7e5afa6a1c050a5d91274bc4f82439fb98640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337961"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a>PidLidEmail2OriginalDisplayName (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den zweiten Anzeigenamen an, der der für den Kontakt angegebenen E-Mail-Adresse entspricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidEmail2OriginalDisplayName  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Lange ID (LID):  <br/> |0x00008094  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn der Wert der **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) -Eigenschaft "SMTP" ist, sollte der Wert der entsprechenden **PidLidEmail2OriginalDisplayName** -Eigenschaft dem Wert der entsprechenden **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) -Eigenschaft entspricht. Der Zweck dieser Eigenschaft besteht in der Anzeige einer alternativen benutzerfreundlichen Adresse, die der in **dispidEmail2EmailAddress entspricht.**
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

