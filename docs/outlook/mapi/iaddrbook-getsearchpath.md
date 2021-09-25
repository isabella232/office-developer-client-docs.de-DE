---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4d4934cb17b66c0daeb09100e024082621555cec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571836"
---
# <a name="iaddrbookgetsearchpath"></a>IAddrBook::GetSearchPath

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine sortierte Liste der Eintragsbezeichner der Container zurück, die in den von der [IAddrBook::ResolveName-Methode](iaddrbook-resolvename.md) initiierten Namensauflösungsprozess einbezogen werden sollen. 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der im Suchpfad zurückgegebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 _lppSearchPath_
  
> [out] Ein Zeiger auf einen Zeiger auf eine sortierte Liste von Containereintragsbezeichnern. **GetSearchPath** speichert die sortierte Liste in einer [SRowSet-Struktur.](srowset.md) Wenn keine Container in der Adressbuchhierarchie vorhanden sind, wird in der **SRowSet-Struktur** Null zurückgegeben. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Suchpfad wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Clients und Dienstanbieter rufen die **GetSearchPath-Methode** auf, um den Suchpfad abzurufen, der zum Auflösen von Namen mit der **ResolveName-Methode** verwendet wird. In der Regel rufen Clients die [IAddrBook::SetSearchPath-Methode](iaddrbook-setsearchpath.md) auf, um einen Containersuchpfad im Profil einzurichten, bevor sie **GetSearchPath** aufrufen, um ihn abzurufen. Das Aufrufen von **SetSearchPath** ist jedoch optional. 
  
Wenn **SetSearchPath** noch nie aufgerufen wurde, erstellt **GetSearchPath** einen Pfad, indem die Hierarchietabellen des Adressbuchs durchgearbeitet werden. Der von **GetSearchPath** erstellte Standardsuchpfad besteht aus den folgenden Containern in der folgenden Reihenfolge: 
  
1. Der erste Container mit Lese-/Schreibberechtigung, in der Regel das persönliche Adressbuch (PAB).
    
2. Jeder Container, dessen **eigenschaft PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) auf DT_GLOBAL festgelegt ist. Diese Einstellung gibt an, dass der Container Empfänger enthält. 
    
3. Der als Standard festgelegte Container, wenn in der **PR_DISPLAY_TYPE-Eigenschaft** kein DT_GLOBAL-Flag festgelegt ist und der Standardcontainer vom ersten Container mit Lese-/Schreibberechtigung abweicht. 
    
Wenn **SetSearchPath** aufgerufen wurde, erstellt **GetSearchPath** einen Pfad mithilfe der Adressbuchcontainer, die im Profil gespeichert wurden. **GetSearchPath** überprüft diesen Pfad, bevor er an den Aufrufer zurückgegeben wird. 
  
Nach dem ersten Aufruf von **SetSearchPath** müssen nachfolgende Aufrufe von **SetSearchPath** verwendet werden, um den von **GetSearchPath** zurückgegebenen Suchpfad zu ändern. Mit anderen Worten, der aufrufende Client oder Anbieter erhält nach dem ersten Aufruf von **SetSearchPath** nicht den Standardsuchpfad.
  
## <a name="see-also"></a>Siehe auch



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

