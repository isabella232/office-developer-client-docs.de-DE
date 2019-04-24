---
title: Kanonische Pidtagservicesupportfiles (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3753177552d45e32e53ae192a9dfae15b601afcc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359472"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a>Kanonische Pidtagservicesupportfiles (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste der Dateien, die zum Nachrichtendienst gehören.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W  <br/> |
|Kennung:  <br/> |0x3D0F  <br/> |
|Datentyp:  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mithilfe eines Dialogfelds in der Systemsteuerung können Benutzer die Liste der Dateien abrufen, die zum Nachrichtendienst gehören. Der Benutzer kann beispielsweise die Namen aller DLLs (Dynamic Link Libraries) abrufen, die zum Dienst gehören. Der Benutzer kann dann zusätzliche Details zu den angegebenen Dateien suchen, beispielsweise die Namen und Versionsnummern aller DLLs. MAPI verwendet die folgenden Eigenschaften zum Erstellen einer Support Dateiliste in einem Dialogfeld für die Auswahl von Messaging Benutzern.
  
MAPI funktioniert nur mit Dateinamen und anderen Zeichenfolgen, die an den Zeichensatz der Active Directory-Dienstschnittstellen (ANSI) übergeben werden. Client Anwendungen, die Dateinamen in einem OEM-Zeichensatz (Original Equipment Manufacturer) verwenden, müssen Sie vor dem Aufrufen von MAPI in ANSI konvertieren.
  
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

