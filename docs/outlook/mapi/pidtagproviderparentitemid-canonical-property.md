---
title: PidTagProviderParentItemId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3a0c8af1cc36fe7f3e4c97023381e0036fed18ed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574818"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a>PidTagProviderParentItemId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Bezeichner für das übergeordnete Element eines Ordners oder eines Elements in einem Speicher an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROVIDER_PARENT_ITEMID  <br/> |
|Kennung:  <br/> |0x0EA4  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI nicht datenübertragungsfähig  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Store Anbieter können einen Wert für diese Eigenschaft für ein übergeordnetes Element eines Ordners oder Elements angeben, aber der Wert sollte zwischen Sitzungen gleich bleiben. Store Anbieter verwenden diese Eigenschaft, um Suchergebnisse zu identifizieren, die von einer Suchmaschine zurückgegeben werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

