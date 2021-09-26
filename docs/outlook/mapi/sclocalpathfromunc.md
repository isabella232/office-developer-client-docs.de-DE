---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7a2638408cad376e2ed9c8f25263a3bf9fa8634b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599018"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht ein lokales Pfad-Gegenstück zum angegebenen UNC-Pfad (Universal Naming Convention). 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a>Parameter

 _szUNC_
  
> [in] Ein Pfad im Format \\ [ _Server_] \[ _Freigabe_] \[ _Pfad_] einer Datei oder eines Verzeichnisses.
    
 _szLocal_
  
> [out] Ein Pfad im Format [ _Laufwerk:_] \[ _Pfad_] derselben Datei oder desselben Verzeichnisses wie für den _szUNC-Parameter._ 
    
 _cchLocal_
  
> [in] Größe des Puffers für die Ausgabezeichenfolge.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Ein lokaler Pfad wurde erfolgreich gefunden.
    
MAPI_E_TOO_BIG
  
>  _szLocal_ war nicht groß genug, um das Ergebnis zu speichern. 
    
S_FALSE
  
> Die UNC-Zeichenfolge war bereits ein lokaler Pfad.
    
MAPI_E_NOT_FOUND
  
> Ein lokaler Pfad wurde nicht gefunden.
    
## <a name="see-also"></a>Siehe auch



[ScUNCFromLocalPath](scuncfromlocalpath.md)

