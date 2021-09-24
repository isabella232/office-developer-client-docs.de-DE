---
title: PidTagDefCreateMailuser (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7734c759fe9b5954dd38ecb74e9423455348fff3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550722"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a>PidTagDefCreateMailuser (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Vorlageneintragsbezeichner für ein standardmäßiges Messagingbenutzerobjekt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEF_CREATE_MAILUSER  <br/> |
|Kennung:  <br/> |0x3612  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Clientanwendungen verwenden diese Eigenschaft, um ein Messagingbenutzerobjekt in einem Container zu erstellen. Die Unterstützung der Erstellung von Einträgen ist für Adressbuchcontainer optional. Diejenigen, die diese Eigenschaft nicht unterstützen, müssen diese Eigenschaft nicht verfügbar machen. 
  
Diese Eigenschaft gibt einen Eintrag an, der in der **eigenschaft PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) für Messagingbenutzer angezeigt werden kann. Nach dem Abrufen des Bezeichners verwendet der Client ihn in einem Aufruf der [IABContainer::CreateEntry-Methode.](iabcontainer-createentry.md) Der Eintrag stellt die Vorlage für den Standardmäßignachrichtenbenutzer dar. 
  
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

