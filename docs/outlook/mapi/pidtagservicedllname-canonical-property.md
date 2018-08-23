---
title: PidTagServiceDllName (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d2917f2119fde38686397b65956113bc430b2e31
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570814"
---
# <a name="pidtagservicedllname-canonical-property"></a>PidTagServiceDllName (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält den Dateinamen der DLL Nachricht Service Provider Entry Point-Funktion, die für die Konfiguration aufrufen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W  <br/> |
|Kennung:  <br/> |0x3D0A  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der Eintrag Punkt Funktionsname in der Methode **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) angezeigt wird, bedeutet dies, dass der Einstiegspunkt vorhanden ist.
  
MAPI verwendet eine DLL-Datei Namenskonvention fest. Die Basis Dateiname enthält maximal sechs Zeichen, die die DLL eindeutig identifizieren. MAPI fügt die Zeichenfolge 32 an den Basisnamen der DLL-Datei zum Ermitteln der Version, die auf 32-Bit-Plattformen ausgeführt wird. Beispielsweise, wenn der Name MAPI. DLL-Datei angegeben wird, MAPI erstellt den Namen MAPI32. DLL, um die entsprechenden 32-Bit-Version der DLL darstellen.
  
Diese Eigenschaften sollten den Basisnamen angeben. MAPI fügt die Zeichenfolge 32 entsprechend an. Einschließlich der Zeichenfolge 32 im Rahmen dieser Eigenschaften führt zu einem Fehler.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[PidTagProviderDllName (kanonische Eigenschaft)](pidtagproviderdllname-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

