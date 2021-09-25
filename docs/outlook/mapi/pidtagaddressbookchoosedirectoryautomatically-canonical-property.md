---
title: PidTagAddressBookChooseDirectoryAutomatically (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 578cdaeaba7ea88249d5f87f5b5ebca2ab28e51d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571248"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>PidTagAddressBookChooseDirectoryAutomatically (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Microsoft Outlook 2010 und Microsoft Outlook 2013, den am besten geeigneten globalen Adresslisten- oder Kontaktordner für das aktuelle Postfach auszuwählen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|Kennung:  <br/> |0x3D1C000B  <br/> |
|Eigenschaftentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft entspricht der Einstellung **"Automatisch auswählen"** im Dialogfeld "Adressbuchoptionen". Wenn diese Eigenschaft im IID_CAPONE_PROF Profilabschnitt vorhanden ist und auf **"true"** festgelegt ist, wird im Adressbuchdialogfeld nicht mehr standardmäßig der von der [SetDefaultDir-Methode](iaddrbook-setdefaultdir.md) angegebene Container verwendet, sondern ein Adressbuch ausgewählt, das Outlook 2010 oder Outlook 2013 für den Kontext geeignet ist, in dem das Dialogfeld angezeigt wurde. Beachten Sie, dass dies zu einer schlechten Erfahrung für Adressbuchanbieter von Drittanbietern führen kann. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

