---
title: Kanonische PidTagResourcePath-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 04ecec1e220af4afcf40fe37fe5e3d90cf943720
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599600"
---
# <a name="pidtagresourcepath-canonical-property"></a>Kanonische PidTagResourcePath-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Pfad zum Server des Dienstanbieters.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W  <br/> |
|Kennung:  <br/> |0x3E07  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der in diesen Eigenschaften enthaltene Pfad stellt den vorgeschlagenen Pfad dar, in dem der Benutzer Ressourcen finden kann. Die Definition dieser Eigenschaften ist anbieterspezifisch. Beispielsweise verwendet eine Planungsanwendung diese Eigenschaften, um den vorgeschlagenen Speicherort für die Planungsanwendungsdateien anzugeben.
  
Das Messaging-Benutzerprofil teilt diese Eigenschaften als Komfort aus, sodass eine Clientanwendung den Messagingbenutzer nicht zur Eingabe eines Netzwerkpfads oder Eines Netzlaufwerkbuchstabens auffordern muss.
  
MAPI funktioniert nur mit Dateinamen im Ansi-Zeichensatz (American National Standards Institute). Anwendungen, die Dateinamen in einem Oem-Zeichensatz (Original Equipment Manufacturer) verwenden, müssen sie vor dem Aufrufen der MAPI in ANSI konvertieren.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

