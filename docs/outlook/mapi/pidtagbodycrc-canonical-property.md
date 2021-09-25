---
title: PidTagBodyCrc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ec43982af01f7329a8cd55e6874ff93ba281cdf8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600407"
---
# <a name="pidtagbodycrc-canonical-property"></a>PidTagBodyCrc (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen CRC-Wert (cyclic redundancy check) für den Nachrichtentext.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_BODY_CRC  <br/> |
|Kennung:  <br/> |0x0E1C  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Nachrichtenspeicher kann einen beliebigen CRC-Algorithmus verwenden, der einen PT_LONG Wert generiert. Sie muss diese Eigenschaft als Teil der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) berechnen, wenn die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft zum ersten Mal festgelegt wurde und wenn sie anschließend geändert wurde.
  
Eine Clientanwendung verwendet **PR_BODY_CRC,** um nachrichtentextzeichenfolgen zu vergleichen, die in **PR_BODY** Eigenschaften oder deren Varianten enthalten sind. Mit dieser Eigenschaft kann der Client schnell und einfach erkennen, wann sich der Nachrichtentext geändert hat. Es kann erhebliche Leistungsvorteile erzielen, indem **PR_BODY_CRC** verwendet wird, anstatt **PR_BODY** aus dem Nachrichtenspeicher zu erhalten und mit einer lokalen Version zu vergleichen. 
  
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

