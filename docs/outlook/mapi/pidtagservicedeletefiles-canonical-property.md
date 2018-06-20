---
title: Kanonische PidTagServiceDeleteFiles-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8f90d72e842df62c19c5aeeaf6c398c5db469560
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795167"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a>Kanonische PidTagServiceDeleteFiles-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine Liste der Dateinamen, die bei der Deinstallation von Message-Dienst gelöscht werden sollen.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W  <br/> |
|Bezeichner:  <br/> |0x3D10  <br/> |
|Datentyp:  <br/> |PT_MV_STRING8 PT_MV_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Hinweise

Die Dateinamen in der Liste in diese Eigenschaften werden vom Computer gelöscht, wenn die Systemsteuerung verwenden, um den Dienst zu deinstallieren. Schließen Sie nicht in der Liste eine DLL, die mehrere Nachrichtendienste für die unterstützt oder zusätzliche Message Dienste konnte versehentlich entfernt.
  
MAPI funktioniert nur mit Dateinamen und andere Zeichenfolgen übergeben wurden, im ANSI-Zeichensatz. Anwendungen, die in einem OEM-Zeichensatz Dateinamen verwenden, müssen diese in ANSI konvertieren, vor dem Aufruf von MAPI.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

