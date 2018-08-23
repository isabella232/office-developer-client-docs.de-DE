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
ms.openlocfilehash: ae1f5b62c59c2e9a1c02c1a2fc0ee91ef1e19387
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562981"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>PidTagWizardNoPstPage (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält True, wenn der Profilassistent die Seite persönliche Nachricht Store (PST) unterdrückt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|Kennung:  <br/> |0x6700  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Exchange-Verwaltung  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dienstanbieter können diese Eigenschaft festlegen, beim Aufrufen einer Funktion basierend auf den [LAUNCHWIZARDENTRY](launchwizardentry.md) Funktionsprototyp. Diese Eigenschaft teilt der Profil-Assistent, dass der Anbieter nicht möchte die PST-Seite, während das Benutzerdialogfeld angezeigt werden soll. 
  
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

