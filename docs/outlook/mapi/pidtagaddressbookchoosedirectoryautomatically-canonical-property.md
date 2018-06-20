---
title: Kanonische PidTagAddressBookChooseDirectoryAutomatically-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 48dfced07a8fd78a1af22679759effbd3c6da343
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794056"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>Kanonische PidTagAddressBookChooseDirectoryAutomatically-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Können Microsoft Outlook 2010 und Microsoft Outlook 2013, zum Auswählen der am besten geeigneten globale Adressliste (GAL) oder Kontakteordner für das aktuelle Postfach.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|Bezeichner:  <br/> |0x3D1C000B  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft entspricht der Einstellung **automatisch wählen Sie** im Dialogfeld Optionen für das Adressbuch. Wenn diese Eigenschaft im Abschnitt IID_CAPONE_PROF Profile vorhanden ist und auf **"true"**, das Adressbuch Dialogfeld nicht mehr standardmäßig auf den Container, die von der [SetDefaultDir](iaddrbook-setdefaultdir.md) -Methode angegeben, aber wählt ein Adressbuch, die festgelegt ist, Outlook 2010 oder Outlook 2013 hält entsprechenden für den Kontext, in dem das Dialogfeld angezeigt wurde. Beachten Sie, dass dies eine schlechte Erfahrung für Drittanbieter-adressbuchanbietern implementierte führen kann. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

