---
title: PidTagDefCreateDl (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 16b9af522adfba01e76a97aeb228c4414b48b79c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550729"
---
# <a name="pidtagdefcreatedl-canonical-property"></a>PidTagDefCreateDl (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Vorlageneintragsbezeichner für eine Standardverteilerliste. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEF_CREATE_DL  <br/> |
|Kennung:  <br/> |0x3611  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Clientanwendungen verwenden diese Eigenschaft, um eine Verteilerliste innerhalb eines Containers zu erstellen. Die Unterstützung der Erstellung von Einträgen ist für Adressbuchcontainer optional. Diejenigen, die diese Eigenschaft nicht unterstützen, müssen diese Eigenschaft nicht verfügbar machen. 
  
Diese Eigenschaft gibt einen Eintrag an, der in der **eigenschaft PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) für Verteilerlisten angezeigt werden kann. Nach dem Abrufen des Bezeichners verwendet der Client ihn in einem Aufruf der [IABContainer::CreateEntry-Methode.](iabcontainer-createentry.md) Der Eintrag stellt die Vorlage für die Standardverteilerliste dar. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

