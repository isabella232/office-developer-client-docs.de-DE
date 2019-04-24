---
title: Kanonische Pidtagwizardnopabpage (-Eigenschaft
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
ms.openlocfilehash: fc971be76dbaa83176f207411f9f125ffee386cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350652"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a>Kanonische Pidtagwizardnopabpage (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält TRUE, wenn der Profil-Assistent die Seite persönliches Adressbuch (PAB) unterdrückt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_WIZARD_NO_PAB_PAGE  <br/> |
|Kennung:  <br/> |0x6701  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Exchange-Verwaltung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dienstanbieter können diese Eigenschaft beim Aufrufen einer Funktion festlegen, die auf dem Prototyp der [LAUNCHWIZARDENTRY](launchwizardentry.md) -Funktion basiert. Diese Eigenschaft teilt dem Profil-Assistenten mit, dass die PAB-Seite im Benutzerdialogfeld nicht angezeigt werden soll. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

