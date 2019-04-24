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
ms.openlocfilehash: b53dd9aaaf18dba5c7e33e0bc7d984de757634a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358772"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht einen UNC-Pfad Gegenstück (Universal Naming Convention) für den angegebenen lokalen Pfad.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a>Parameter

 _szLocal_
  
> in Ein Pfad im Format [ _Drive:_]\[ _path_] einer Datei oder eines Verzeichnisses.
    
 _szUNC_
  
> Out Ein Pfad im \\Format [ _Server_]\[ _Freigabe_\[ _Pfad_] derselben Datei oder desselben Verzeichnisses wie für den _szLocal_ -Parameter. 
    
 _cchUNC_
  
> in Die Größe des Puffers für die Ausgabezeichenfolge.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der UNC-Pfad Gegenstück wurde erfolgreich gefunden.
    
MAPI_E_INVALID_PARAMETER
  
> Mindestens ein Parameter ist ungültig.
    
MAPI_E_TOO_BIG
  
>  _szUNC_ war nicht groß genug, um das Ergebnis zu halten. 
    
S_FALSE
  
> Der lokale Pfad war bereits eine UNC-Zeichenfolge.
    
## <a name="see-also"></a>Siehe auch



[ScLocalPathFromUNC](sclocalpathfromunc.md)

