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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2dc431d807bd74640e5b5a9c020f668b13530197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795191"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a>PidTagServiceSupportFiles (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine Liste der Dateien, die den Dienst angehören.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W  <br/> |
|Bezeichner:  <br/> |0x3D0F  <br/> |
|Datentyp:  <br/> |PT_MV_STRING8 PT_MV_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mithilfe eines Dialogfelds in der Systemsteuerungsoption, kann ein Benutzer die Liste der Dateien erhalten, die den Dienst angehören. Beispielsweise kann der Benutzer die Namen der alle Dynamic Link Libraries (DLLs) abgerufen, die mit dem Dienst gehören. Der Benutzer kann dann zusätzliche Informationen zu der angegebenen Dateien, beispielsweise den Namen und die Versionsnummern aller DLLs seek. MAPI verwendet diese Eigenschaften zum Erstellen einer Support-Datei-Liste in einem Dialogfeld für die Auswahl des Benutzers messaging.
  
MAPI funktioniert nur mit Dateinamen und andere Zeichenfolgen übergeben wurden, in den Zeichensatz für die Active Directory Service Interfaces (ANSI). Clientanwendungen, die Dateinamen in einem Zeichensatz OEM (Original Equipment Manufacturer) verwenden, müssen sie in ANSI zu konvertieren vor dem Aufruf von MAPI.
  
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

