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
ms.openlocfilehash: adf24bcd02d7efc303f911ee01a64325150339ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330065"
---
# <a name="pidtagservicedllname-canonical-property"></a>PidTagServiceDllName (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Dateinamen der DLL, die die Einstiegspunktfunktion des Nachrichtendienstanbieters zum Aufrufen der Konfiguration enthält.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W  <br/> |
|Kennung:  <br/> |0x3D0A  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn der Name der Einstiegspunktfunktion in der **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) -Methode angezeigt wird, gibt er an, dass der Einstiegspunkt vorhanden ist.
  
MAPI verwendet eine DLL-Dateibenennungskonvention. Sie fügt die Zeichenfolge 32 an den Basis-DLL-Namen an, um die Version zu identifizieren, die auf 32-Bit-Plattformen ausgeführt wird. Wenn beispielsweise der Name MAPI.DLL angegeben wird, erstellt MAPI den Namen MAPI32.DLL, um die entsprechende 32-Bit-Version der DLL zu repräsentieren.
  
Diese Eigenschaften sollten den Basisnamen angeben. MAPI fügt die Zeichenfolge 32 an. Das Einschleingen der Zeichenfolge 32 als Teil dieser Eigenschaften führt zu einem Fehler.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagProviderDllName (kanonische Eigenschaft)](pidtagproviderdllname-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

