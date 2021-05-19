---
title: PidTagAddressBookChooseDirectoryAutomatically Canonical Property
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 41fdaf333084b7d567f4e67ae9fd2638a1731349
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409664"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>PidTagAddressBookChooseDirectoryAutomatically Canonical Property

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Microsoft Outlook 2010 und Microsoft Outlook 2013, die am besten geeignete globale Adressliste (GAL) oder den Kontaktordner für das aktuelle Postfach zu wählen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|Kennung:  <br/> |0x3D1C000B  <br/> |
|Eigenschaftstyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft entspricht der Einstellung **Automatisch auswählen** im Dialogfeld Adressbuchoptionen. Wenn diese Eigenschaft im Abschnitt IID_CAPONE_PROF-Profil vorhanden ist und auf **true** festgelegt ist, wird im Adressbuchdialogfeld nicht mehr standardmäßig der von der [SetDefaultDir-Methode](iaddrbook-setdefaultdir.md) angegebene Container verwendet, sondern ein Adressbuch ausgewählt, das Outlook 2010 oder Outlook 2013 für den Kontext geeignet ist, in dem das Dialogfeld angezeigt wurde. Beachten Sie, dass dies zu einer schlechten Erfahrung für Adressbuchanbieter von Drittanbietern führen kann. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

