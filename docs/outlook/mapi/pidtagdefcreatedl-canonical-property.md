---
title: PidTagDefCreateDl (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ff5d35104e9effc27c405b716cb61cf4643677b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417791"
---
# <a name="pidtagdefcreatedl-canonical-property"></a>PidTagDefCreateDl (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Vorlageneintrags-ID für eine Standardverteilungsliste. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEF_CREATE_DL  <br/> |
|Kennung:  <br/> |0x3611  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Clientanwendungen verwenden diese Eigenschaft, um eine Verteilerliste innerhalb eines Containers zu erstellen. Die Unterstützung der Eintragserstellung ist für Adressbuchcontainer optional. Diejenigen, die sie nicht unterstützen, müssen diese Eigenschaft nicht verfügbar machen. 
  
Diese Eigenschaft gibt einen Eintrag an, der in der **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) -Eigenschaft für Verteilerlisten angezeigt werden kann. Nach dem Abrufen des Bezeichners verwendet der Client ihn in einem Aufruf der [IABContainer::CreateEntry-Methode.](iabcontainer-createentry.md) Der Eintrag stellt die Vorlage für die Standardverteilungsliste dar. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

