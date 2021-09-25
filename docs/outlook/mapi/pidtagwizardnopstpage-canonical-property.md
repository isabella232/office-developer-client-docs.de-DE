---
title: PidTagWizardNoPstPage (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagWizardNoPstPage
api_type:
- COM
ms.assetid: 1ac09578-892b-4c72-92f6-c2419ac2efe8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bcf42991c31cfb7313ee1a668b5423db1defbe33
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586866"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>PidTagWizardNoPstPage (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält TRUE, wenn der Profil-Assistent die PsT-Seite (Personal Message Store) unterdrücken soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|Kennung:  <br/> |0x6700  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Exchange Administrative  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dienstanbieter können diese Eigenschaft festlegen, wenn sie eine Funktion aufrufen, die auf dem Prototyp der [LAUNCHWIZARDENTRY-Funktion](launchwizardentry.md) basiert. Diese Eigenschaft teilt dem Profil-Assistenten mit, dass der Anbieter nicht möchte, dass die PST-Seite während des Benutzerdialogs angezeigt wird. 
  
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

