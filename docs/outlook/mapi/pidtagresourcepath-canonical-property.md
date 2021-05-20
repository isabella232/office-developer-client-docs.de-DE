---
title: PidTagResourcePath (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 32d150e508f5c208e15d5ee5f0b8c800a1e597f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429859"
---
# <a name="pidtagresourcepath-canonical-property"></a>PidTagResourcePath (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Pfad zum Server des Dienstanbieters.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W  <br/> |
|Kennung:  <br/> |0x3E07  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Hinweise

Der in diesen Eigenschaften enthaltene Pfad stellt den vorgeschlagenen Pfad dar, in dem der Benutzer Ressourcen finden kann. Die Definition dieser Eigenschaften ist anbieterspezifisch. Beispielsweise verwendet eine Planungsanwendung diese Eigenschaften, um den vorgeschlagenen Speicherort für die Planungsanwendungsdateien anzugeben.
  
Das Messagingbenutzerprofil bietet diese Eigenschaften als Komfort, sodass eine Clientanwendung den Messagingbenutzer nicht zur Eingabe eines Netzwerkpfads oder Eines Netzlaufwerkbuchstabens anfordern muss.
  
MAPI kann nur mit Dateinamen im Zeichensatz American National Standards Institute (ANSI) verwendet werden. Anwendungen, die Dateinamen in einem OEM-Zeichensatz (Original Equipment Manufacturer) verwenden, müssen sie vor dem Aufrufen von MAPI in ANSI konvertieren.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

