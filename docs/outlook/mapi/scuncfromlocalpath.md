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
ms.openlocfilehash: faba91d813d27f7ea45e978724ce0d4707803cba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590106"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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

