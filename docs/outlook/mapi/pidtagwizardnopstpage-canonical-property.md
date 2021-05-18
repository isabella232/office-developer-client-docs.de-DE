---
title: PidTagWizardNoPstPage (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPstPage
api_type:
- COM
ms.assetid: 1ac09578-892b-4c72-92f6-c2419ac2efe8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e816af2ce60b4c06ae14f720cf7c36d58468d09d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422887"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>PidTagWizardNoPstPage (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält TRUE, wenn der Profil-Assistent die Seite für den persönlichen Nachrichtenspeicher (PST) unterdrücken soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|Kennung:  <br/> |0x6700  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Exchange Administrative  <br/> |
   
## <a name="remarks"></a>Hinweise

Dienstanbieter können diese Eigenschaft beim Aufrufen einer Funktion basierend auf dem PROTOTYP der [LAUNCHWIZARDENTRY-Funktion](launchwizardentry.md) festlegen. Diese Eigenschaft teilt dem Profil-Assistenten mit, dass der Anbieter nicht möchte, dass die PST-Seite während des Benutzerdialogfelds angezeigt wird. 
  
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

