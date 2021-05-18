---
title: PidTagDefCreateMailuser (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cd09c85e4f44bbea29807d72a273ccf6980ca6df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407480"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a>PidTagDefCreateMailuser (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Vorlageneintrags-ID für ein Standardmäßiges Messagingbenutzerobjekt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEF_CREATE_MAILUSER  <br/> |
|Kennung:  <br/> |0x3612  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Clientanwendungen verwenden diese Eigenschaft, um ein Messagingbenutzerobjekt in einem Container zu erstellen. Die Unterstützung der Eintragserstellung ist für Adressbuchcontainer optional. Diejenigen, die sie nicht unterstützen, müssen diese Eigenschaft nicht verfügbar machen. 
  
Diese Eigenschaft gibt einen Eintrag an, der in der **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) -Eigenschaft für Messagingbenutzer angezeigt werden kann. Nach dem Abrufen des Bezeichners verwendet der Client ihn in einem Aufruf der [IABContainer::CreateEntry-Methode.](iabcontainer-createentry.md) Der Eintrag stellt die Vorlage für den Standardnachrichtenbenutzer dar. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

