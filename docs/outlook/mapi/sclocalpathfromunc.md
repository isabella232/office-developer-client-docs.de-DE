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
ms.openlocfilehash: e303361f4f0dd3a08dbb362096d07b8b391a6d97
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594418"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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

