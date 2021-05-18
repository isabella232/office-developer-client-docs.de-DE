---
title: PidTagProviderDllName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDllName
api_type:
- COM
ms.assetid: 9ddb38eb-9a32-4dbe-b42c-6ea9db98acd2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 57fdc754ed4be29dbdd50a198707d8f39a14b3d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286488"
---
# <a name="pidtagproviderdllname-canonical-property"></a>PidTagProviderDllName (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Basisdateinamen der DLL (Dynamic Link Library) des MAPI-Dienstanbieters.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W  <br/> |
|Kennung:  <br/> |0x300A  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI allgemein  <br/> |
   
## <a name="remarks"></a>Hinweise

MAPI verwendet eine DLL-Dateibenennungskonvention. Sie fügt die Zeichenfolge 32 an den Basis-DLL-Namen an, um die Version zu identifizieren, die auf 32-Bit-Plattformen ausgeführt wird. Wenn beispielsweise der Name MAPI.DLL angegeben wird, erstellt MAPI den Namen MAPI32.DLL, um die entsprechende 32-Bit-Version der DLL zu repräsentieren.
  
Diese Eigenschaften sollten den Basisnamen angeben. MAPI fügt die Zeichenfolge 32 an. Das Angeben der Zeichenfolge 32 als Teil dieser Eigenschaft führt zu einem Fehler.
  
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

