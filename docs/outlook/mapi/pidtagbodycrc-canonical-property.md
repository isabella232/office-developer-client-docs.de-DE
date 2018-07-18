---
title: PidTagBodyCrc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 66a150cf3f83465840aa0e79a9ef921b1534f814
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794152"
---
# <a name="pidtagbodycrc-canonical-property"></a>PidTagBodyCrc (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält einen CRC CRC-Prüfung Wert auf den Nachrichtentext an.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_BODY_CRC  <br/> |
|Bezeichner:  <br/> |0x0E1C  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Nachrichtenspeicher können jeder CRC-Algorithmus, der einen PT_LONG Wert generiert. Es muss diese Eigenschaft als Teil der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode berechnen, wenn die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft festgelegt wurde, zum ersten Mal und wenn es später geändert wurde.
  
Eine Clientanwendung verwendet **PR_BODY_CRC** zur Unterstützung bei der vergleichen Nachricht Textzeichenfolgen in **PR_BODY** Eigenschaften oder deren Varianten enthalten. Mithilfe dieser Eigenschaft, kann der Client schnell und einfach erkennen, wann der Nachrichtentext geändert hat. Es kann erhebliche Leistungssteigerungen Realisierung von über **PR_BODY_CRC** anstatt **PR_BODY** aus dem Nachrichtenspeicher abrufen und diese mit einer lokalen Version zu vergleichen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

