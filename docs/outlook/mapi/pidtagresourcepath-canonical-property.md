---
title: Kanonische Pidtagresourcepath (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 32d150e508f5c208e15d5ee5f0b8c800a1e597f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330170"
---
# <a name="pidtagresourcepath-canonical-property"></a>Kanonische Pidtagresourcepath (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Pfad zum Server des Dienstanbieters.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W  <br/> |
|Kennung:  <br/> |0x3E07  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der in diesen Eigenschaften enthaltene Pfad stellt den vorgeschlagenen Pfad dar, in dem der Benutzer Ressourcen finden kann. Die Definition dieser Eigenschaften ist Anbieter spezifisch. Eine Planungsanwendung verwendet diese Eigenschaften zum Beispiel, um den vorgeschlagenen Speicherort für die Planungs Anwendungsdateien anzugeben.
  
Das Messaging-Benutzerprofil stellt diese Eigenschaften als Bequemlichkeit bereit, sodass eine Clientanwendung den Messagingbenutzer nicht für einen Netzwerkpfad oder Netzlaufwerkbuchstaben auffordern muss.
  
MAPI funktioniert nur mit Dateinamen im ANSI-Zeichensatz (American National Standards Institute). Anwendungen, die Dateinamen in einem OEM-Zeichensatz (Original Equipment Manufacturer) verwenden, müssen Sie vor dem Aufrufen von MAPI in ANSI konvertieren.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

