---
title: Kanonische Pidtagaddressbookchoosedirectoryautomatically (-Eigenschaft
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
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>Kanonische Pidtagaddressbookchoosedirectoryautomatically (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Microsoft Outlook 2010 und Microsoft Outlook 2013, die am besten geeignete globale Adressliste (GAL) oder den Kontaktordner für das aktuelle Postfach auszuwählen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|Kennung:  <br/> |0x3D1C000B  <br/> |
|Eigenschafts:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft entspricht der Einstellung **automatisch auswählen** im Dialogfeld Adressbuchoptionen. Wenn diese Eigenschaft im Abschnitt IID_CAPONE_PROF vorhanden ist und auf **true**festgelegt ist, ist das Adressbuch-Dialogfeld nicht mehr standardmäßig der Container von der [SetDefaultDir](iaddrbook-setdefaultdir.md) -Methode angegeben, aber wählt ein adressbuch, outlook 2010 oder Outlook 2013 ist für den Kontext geeignet, in dem das Dialogfeld angezeigt wurde. Beachten Sie, dass dies zu einer schlechten Erfahrung für Drittanbieter-Adressbuchanbieter führen kann. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header Dateien

Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

