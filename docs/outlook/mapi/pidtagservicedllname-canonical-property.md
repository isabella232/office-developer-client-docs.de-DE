---
title: Kanonische Pidtagservicedllname (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDllName
api_type:
- COM
ms.assetid: a651af84-1711-449e-ba7e-5ce09cafa02b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: adf24bcd02d7efc303f911ee01a64325150339ce
ms.sourcegitcommit: 18f3d9462048859fe040e12136ff66f19066764b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2019
ms.locfileid: "31980454"
---
# <a name="pidtagservicedllname-canonical-property"></a>Kanonische Pidtagservicedllname (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Dateinamen der DLL mit der Einstiegspunktfunktion des Nachrichtendienst Anbieters, die für die Konfiguration aufgerufen werden soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W  <br/> |
|Kennung:  <br/> |0x3D0A  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn der Name der Einstiegspunktfunktion in der **PR_SERVICE_ENTRY_NAME** ([pidtagserviceentryname (](pidtagserviceentryname-canonical-property.md))-Methode angezeigt wird, gibt er an, dass der Einstiegspunkt vorhanden ist.
  
MAPI verwendet eine Benennungskonvention für DLL-Dateien. Sie fügt die Zeichenfolge 32 an den Basis-DLL-Namen an, um die Version zu identifizieren, die auf 32-Bit-Plattformen ausgeführt wird. Wenn beispielsweise der Name "MAPI" lautet. DLL angegeben ist, erstellt MAPI den Namen MAPI32. DLL zur Darstellung der entsprechenden 32-Bit-Version der DLL.
  
Diese Eigenschaften sollten den Basisnamen angeben. MAPI fügt die Zeichenfolge 32 entsprechend an. Das Einschließen der Zeichenfolge 32 als Teil dieser Eigenschaften führt zu einem Fehler.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagproviderdllname (-Eigenschaft](pidtagproviderdllname-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

