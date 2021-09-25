---
title: Kanonische PidLidAnniversaryEventEntryId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAnniversaryEventEntryId
api_type:
- COM
ms.assetid: 177b2b87-7a06-4d53-8f03-5bec5632c2dd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9de7bf8d2325b49a643122ddcba251b727965bdb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567123"
---
# <a name="pidlidanniversaryevententryid-canonical-property"></a>Kanonische PidLidAnniversaryEventEntryId-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Eintragsbezeichner des Termins an, der den Jahrestag des Kontakts darstellt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidAnniversaryEventEID  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x0000804E  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der durch die **dispidAnniversaryEventEID-Eigenschaft** angegebene Termin muss mithilfe der Eigenschaften **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) und **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) mit diesem Kontakt verknüpft werden, wie in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)beschrieben.
  
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

