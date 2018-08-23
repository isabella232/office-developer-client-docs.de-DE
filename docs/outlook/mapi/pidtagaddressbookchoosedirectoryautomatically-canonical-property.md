---
title: PidTagAddressBookChooseDirectoryAutomatically (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b685fd0ebe4a2d0bfcfd8aab3015602b84932db7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564941"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>PidTagAddressBookChooseDirectoryAutomatically (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Können Microsoft Outlook 2010 und Microsoft Outlook 2013, zum Auswählen der am besten geeigneten globale Adressliste (GAL) oder Kontakteordner für das aktuelle Postfach.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|Kennung:  <br/> |0x3D1C000B  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

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

