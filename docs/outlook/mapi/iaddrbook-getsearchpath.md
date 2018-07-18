---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c20cd7f82df2fb7f878db177fdc940022e1da351
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792005"
---
# <a name="iaddrbookgetsearchpath"></a>IAddrBook::GetSearchPath

  
  
**Betrifft**: Outlook 
  
Gibt eine geordnete Liste von Eintrags-IDs der Container in der [IAddrBook::ResolveName](iaddrbook-resolvename.md) -Methode initiiert Vorgang der Lösung enthalten sein. 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ der Zeichenfolgen steuert, die in den Suchpfad zurückgegeben. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 _lppSearchPath_
  
> [out] Ein Zeiger auf einen Zeiger auf eine sortierte Liste der Container-Eintragsbezeichner. **GetSearchPath** speichert die sortierte Liste in eine [SRowSet](srowset.md) -Struktur. Wenn keine Container in der Adressbuchhierarchie vorhanden sind, wird 0 (null) in der Struktur **SRowSet** zurückgegeben. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Suchpfad wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Clients und Dienstanbieter rufen Sie die **GetSearchPath-** Methode, um den Suchpfad abzurufen, der zum Auflösen von Namen mit der **ResolveName** -Methode verwendet wird. In der Regel rufen Clients die [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) -Methode, um einen Container Suchpfad im Profil herzustellen, vor dem Aufruf von **GetSearchPath** , um sie abzurufen. Aufrufen von **SetSearchPath** ist jedoch optional. 
  
Wenn **SetSearchPath** noch nie aufgerufen wurde, werden erstellt **GetSearchPath** einen Pfad durcharbeiten die Adresse des Buchs Hierarchietabellen. Der Standardsuchpfad **GetSearchPath** eingesetzten umfasst die folgenden Container in der folgenden Reihenfolge: 
  
1. Der erste Container mit Lese-/Schreibzugriff, normalerweise über das persönliche Adressbuch (PAB).
    
2. Jedes Container, dessen **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))-Eigenschaft auf DT_GLOBAL festgelegt ist. Diese Einstellung gibt an, dass der Container Empfänger enthält. 
    
3. Der Container als Standard, festgelegt werden, wenn es sind keine Container, die die in ihrer **PR_DISPLAY_TYPE** -Eigenschaft und der Standardcontainer DT_GLOBAL gekennzeichnet sind unterscheidet sich von den ersten Container mit Lese-/Schreibzugriff. 
    
Wenn **SetSearchPath** aufgerufen wurde, erstellt **GetSearchPath** einen Pfad mit Address Book Container, die im Profil gespeichert wurden. **GetSearchPath** überprüft dieser Pfad, bevor sie ihn an den Aufrufer zurückgibt. 
  
Nach dem ersten Aufruf von **SetSearchPath**müssen nachfolgende Aufrufe von **SetSearchPath** so ändern Sie den zurückgegebene **GetSearchPath**Suchpfad verwendet werden. Anders ausgedrückt, erhält die aufrufende Client oder Anbieter den Standardpfad für die Suche nach dem ersten Aufruf von **SetSearchPath**keine.
  
## <a name="see-also"></a>Siehe auch



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

