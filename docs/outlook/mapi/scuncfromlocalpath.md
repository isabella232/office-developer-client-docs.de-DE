---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4cb47ae7f880985c625e61a4ca6fc02ba1477441
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591192"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht eine UNC-Pfad-Entsprechung (Universal Naming Convention) zum angegebenen lokalen Pfad.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a>Parameter

 _szLocal_
  
> [in] Ein Pfad im Format [ _Laufwerk:_] \[ _Pfad_] einer Datei oder eines Verzeichnisses.
    
 _szUNC_
  
> [out] Ein Pfad im Format \\ [ _Server_] \[ _Freigabe_] \[ _Pfad_] derselben Datei oder desselben Verzeichnisses wie für den _parameter szLocal._ 
    
 _cchUNC_
  
> [in] Größe des Puffers für die Ausgabezeichenfolge.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Die ENTC-Pfad-Entsprechung wurde erfolgreich gefunden.
    
MAPI_E_INVALID_PARAMETER
  
> Mindestens ein Parameter ist ungültig.
    
MAPI_E_TOO_BIG
  
>  _szUNC_ war nicht groß genug, um das Ergebnis zu speichern. 
    
S_FALSE
  
> Der lokale Pfad war bereits eine UNC-Zeichenfolge.
    
## <a name="see-also"></a>Siehe auch



[ScLocalPathFromUNC](sclocalpathfromunc.md)

