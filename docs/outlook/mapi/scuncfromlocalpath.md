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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 667eda2a018d2a5d712950a31e05ec0ba9bb32ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795472"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**Betrifft**: Outlook 
  
Sucht nach einer universal naming Convention (UNC) Pfad Entsprechung für den angegebenen lokalen Pfad.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a>Parameter

 _szLocal_
  
> [in] Einen Pfad im Format [ _Laufwerk:_]\[ _Pfad_] einer Datei oder ein Verzeichnis.
    
 _szUNC_
  
> [out] Einen Pfad im Format \\[ _Server_]\[ _Freigeben_]\[ _Pfad_] der gleichen Datei oder des Verzeichnisses wie bei der _SzLocal_ -Parameter. 
    
 _cchUNC_
  
> [in] Die Größe des Puffers für die Ausgabezeichenfolge.
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Das Gegenstück der UNC-Pfad wurde erfolgreich gefunden.
    
MAPI_E_INVALID_PARAMETER
  
> Ein oder mehrere Parameter sind ungültig.
    
MAPI_E_TOO_BIG
  
>  _SzUNC_ war nicht groß genug für das Ergebnis. 
    
S_FALSE
  
> Der lokale Pfad wurde bereits eine UNC-Zeichenfolge.
    
## <a name="see-also"></a>Siehe auch



[ScLocalPathFromUNC](sclocalpathfromunc.md)

