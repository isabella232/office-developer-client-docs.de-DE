---
title: PidTagWizardNoPabPage (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagWizardNoPabPage
api_type:
- COM
ms.assetid: 9cec22cd-798d-41f6-9ebd-c7354f2162c2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f66afac0d76705eb2a7910310626097cd2c5e2ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599263"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a>PidTagWizardNoPabPage (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält TRUE, wenn der Profil-Assistent die PAB-Seite (Personal Address Book) unterdrücken soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_WIZARD_NO_PAB_PAGE  <br/> |
|Kennung:  <br/> |0x6701  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Exchange Administrative  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dienstanbieter können diese Eigenschaft festlegen, wenn sie eine Funktion aufrufen, die auf dem Prototyp der [LAUNCHWIZARDENTRY-Funktion](launchwizardentry.md) basiert. Diese Eigenschaft teilt dem Profil-Assistenten mit, dass der Anbieter nicht möchte, dass die PAB-Seite während des Benutzerdialogs angezeigt wird. 
  
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

