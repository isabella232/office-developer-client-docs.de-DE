---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e7607a57da5b618a20d6c8e360c7e3cb4f933856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432233"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht ein lokales Pfad-Gegenstück zum angegebenen Unc-Pfad (Universal Naming Convention). 
  
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
  
> [in] Ein Pfad im Format \\ [ _server_] \[ _share_] \[ _path_] einer Datei oder eines Verzeichnisses.
    
 _szLocal_
  
> [out] Ein Pfad im Format [ _drive:_] path ] derselben Datei oder desselben Verzeichnisses \[ wie für den _szUNC-Parameter._ 
    
 _cchLocal_
  
> [in] Größe des Puffers für die Ausgabezeichenfolge.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Ein lokaler Pfad wurde erfolgreich lokalisiert.
    
MAPI_E_TOO_BIG
  
>  _szLocal war_ nicht groß genug, um das Ergebnis zu halten. 
    
S_FALSE
  
> Die UNC-Zeichenfolge war bereits ein lokaler Pfad.
    
MAPI_E_NOT_FOUND
  
> Ein lokaler Pfad wurde nicht gefunden.
    
## <a name="see-also"></a>Siehe auch



[ScUNCFromLocalPath](scuncfromlocalpath.md)

