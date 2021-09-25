---
title: PidTagServiceSupportFiles (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagServiceSupportFiles
api_type:
- COM
ms.assetid: df4be986-62a8-49d6-8eca-25b55c74f830
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dd735eccd7dcfc9d9dd86c3af31aa00a899b561d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586894"
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Mithilfe eines Dialogfelds im Systemsteuerungs-Applet kann ein Benutzer die Liste der Dateien abrufen, die zum Nachrichtendienst gehören. Beispielsweise kann der Benutzer die Namen aller DlLs (Dynamic Link Libraries) abrufen, die zum Dienst gehören. Der Benutzer kann dann weitere Details zu den angegebenen Dateien, z. B. die Namen und Versionsnummern aller DLLs, anfordern. MAPI verwendet diese Eigenschaften, um eine Supportdateiliste in einem Dialogfeld für die Auswahl von Messagingbenutzern zu erstellen.
  
MAPI funktioniert nur mit Dateinamen und anderen Zeichenfolgen, die an sie übergeben werden, im Active Directory Service Interfaces (ANSI)-Zeichensatz. Clientanwendungen, die Dateinamen in einem Oem-Zeichensatz (Original Equipment Manufacturer) verwenden, müssen sie vor dem Aufrufen der MAPI in ANSI konvertieren.
  
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

