---
title: PidTagProviderParentItemId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 96a9d153fadbe8b4c8baa8532b8c99771b1d7987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794833"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a>PidTagProviderParentItemId (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt einen Bezeichner für das übergeordnete Objekt eines Ordners oder eines Elements in einem Speicher an.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_PROVIDER_PARENT_ITEMID  <br/> |
|Bezeichner:  <br/> |0x0EA4  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI Übertragungseinehit  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Anbieter können, geben Sie einen Wert für diese Eigenschaft für ein übergeordnetes Element eines Ordners oder ein Element, jedoch sollten behalten Sie den Wert zwischen Sitzungen identisch. Anbieter mit dieser Eigenschaft können Sie um Suchergebnisse aus einer Suchmaschine zu identifizieren.
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

