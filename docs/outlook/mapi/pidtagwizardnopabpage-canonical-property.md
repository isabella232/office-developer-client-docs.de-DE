---
title: PidTagWizardNoPabPage (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPabPage
api_type:
- COM
ms.assetid: 9cec22cd-798d-41f6-9ebd-c7354f2162c2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b393155d00b47fa8cce23c1b5ac7043237a58983
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795312"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a>PidTagWizardNoPabPage (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Diese Eigenschaft enthält True, wenn der Profilassistent unterdrückt werden, die Seite Persönliches Adressbuch (PAB).
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_WIZARD_NO_PAB_PAGE  <br/> |
|Bezeichner:  <br/> |0x6701  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Exchange-Verwaltung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dienstanbieter können diese Eigenschaft festlegen, beim Aufrufen einer Funktion basierend auf den [LAUNCHWIZARDENTRY](launchwizardentry.md) Funktionsprototyp. Diese Eigenschaft teilt der Profil-Assistent, dass der Anbieter nicht möchte die PAB-Seite, während das Benutzerdialogfeld angezeigt werden soll. 
  
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

