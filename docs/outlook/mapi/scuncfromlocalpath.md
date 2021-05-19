---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b53dd9aaaf18dba5c7e33e0bc7d984de757634a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414536"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht eine Unc-Pfad-Entsprechung (Universal Naming Convention) zum angegebenen lokalen Pfad.
  
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
  
> [out] Ein Pfad im Format [ server ] share ] path ] derselben Datei oder desselben Verzeichnisses \\ wie für den  \[  \[  _szLocal-Parameter._ 
    
 _cchUNC_
  
> [in] Größe des Puffers für die Ausgabezeichenfolge.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Die Entsprechung für den UNC-Pfad wurde erfolgreich auf dem Entsprechendenpfad befindet.
    
MAPI_E_INVALID_PARAMETER
  
> Mindestens ein Parameter ist ungültig.
    
MAPI_E_TOO_BIG
  
>  _szUNC war_ nicht groß genug, um das Ergebnis zu halten. 
    
S_FALSE
  
> Der lokale Pfad war bereits eine UNC-Zeichenfolge.
    
## <a name="see-also"></a>Siehe auch



[ScLocalPathFromUNC](sclocalpathfromunc.md)

