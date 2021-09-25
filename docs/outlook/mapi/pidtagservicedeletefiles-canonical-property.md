---
title: PidTagServiceDeleteFiles (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bd1806de1e4077a8057a0ae14b3a07bae87bc6b2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591437"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a>PidTagServiceDeleteFiles (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste der Dateinamen, die gelöscht werden sollen, wenn der Nachrichtendienst deinstalliert wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W  <br/> |
|Kennung:  <br/> |0x3D10  <br/> |
|Datentyp:  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Dateinamen in der Liste, die in diesen Eigenschaften enthalten sind, werden vom Computer gelöscht, wenn die Systemsteuerung zum Deinstallieren des Nachrichtendiensts verwendet wird. Fügen Sie keine DLL in die Liste ein, die mehrere Nachrichtendienste unterstützt, oder zusätzliche Nachrichtendienste könnten versehentlich entfernt werden.
  
MAPI funktioniert nur mit Dateinamen und anderen Zeichenfolgen, die an sie übergeben werden, im ANSI-Zeichensatz. Anwendungen, die Dateinamen in einem OEM-Zeichensatz verwenden, müssen sie vor dem Aufrufen der MAPI in ANSI konvertieren.
  
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

