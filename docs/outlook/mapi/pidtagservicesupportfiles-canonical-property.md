---
title: PidTagServiceSupportFiles (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceSupportFiles
api_type:
- COM
ms.assetid: df4be986-62a8-49d6-8eca-25b55c74f830
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3753177552d45e32e53ae192a9dfae15b601afcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417042"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a>PidTagServiceSupportFiles (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste der Dateien, die zum Nachrichtendienst gehören.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W  <br/> |
|Kennung:  <br/> |0x3D0F  <br/> |
|Datentyp:  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Hinweise

Mithilfe eines Dialogfelds im Systemsteuerungs-Applet kann ein Benutzer die Liste der Dateien abrufen, die zum Nachrichtendienst gehören. Beispielsweise kann der Benutzer die Namen aller Dynamic Link Libraries (DLLs) abrufen, die zum Dienst gehören. Der Benutzer kann dann zusätzliche Details zu den angegebenen Dateien einsuchen, z. B. die Namen und Versionsnummern aller DLLs. MAPI verwendet diese Eigenschaften, um eine Unterstützungsdateiliste in einem Dialogfeld für die Auswahl von Messagingbenutzern zu erstellen.
  
MAPI funktioniert nur mit Dateinamen und anderen Zeichenfolgen, die an sie übergeben werden, im Active Directory Service Interfaces (ANSI)-Zeichensatz. Clientanwendungen, die Dateinamen in einem Oem-Zeichensatz (Original Equipment Manufacturer) verwenden, müssen sie vor dem Aufrufen von MAPI in ANSI konvertieren.
  
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

