---
title: PidTagOwnStoreEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOwnStoreEntryId
api_type:
- COM
ms.assetid: 6a82ee90-10a1-49e0-8f3a-a2cd9f490f99
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: af4f4776a97104f0bcf47681195048fce27687d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574923"
---
# <a name="pidtagownstoreentryid-canonical-property"></a>PidTagOwnStoreEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Eintragsbezeichner des eng gekoppelten Nachrichtenspeichers eines Transports.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_OWN_STORE_ENTRYID  <br/> |
|Kennung:  <br/> |0x3E06  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Nachrichteneigenschaften Store  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft gibt den Eintragsbezeichner für den eng gekoppelten Speicher an, sofern vorhanden. Beispielsweise kann ein Transportanbieter den Eintragsbezeichner für den privaten Ordnerspeicher angeben, damit der MAPI-Spooler den Transportanbieter mit dem Speicher verbinden kann.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

