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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e94692ac4eb401109fcb522e6224c8748bef37f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795456"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**Betrifft**: Outlook 
  
Sucht nach einem Gegenstück lokaler Pfad zu dem angegebenen Pfad universal naming Convention (UNC). 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a>Parameter

 _szUNC_
  
> [in] Einen Pfad im Format \\[ _Server_]\[ _Freigeben_]\[ _Pfad_] einer Datei oder ein Verzeichnis.
    
 _szLocal_
  
> [out] Einen Pfad im Format [ _Laufwerk:_]\[ _Pfad_] der gleichen Datei oder des Verzeichnisses wie bei der _SzUNC_ -Parameter. 
    
 _cchLocal_
  
> [in] Die Größe des Puffers für die Ausgabezeichenfolge.
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Lokaler Pfad wurde erfolgreich gefunden.
    
MAPI_E_TOO_BIG
  
>  _SzLocal_ war nicht groß genug für das Ergebnis. 
    
S_FALSE
  
> Die Zeichenfolge UNC war bereits ein lokaler Pfad.
    
MAPI_E_NOT_FOUND
  
> Lokaler Pfad wurde nicht gefunden.
    
## <a name="see-also"></a>Siehe auch



[ScUNCFromLocalPath](scuncfromlocalpath.md)

