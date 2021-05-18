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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f8c129e772870804ef464765b2035a3582317a09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412982"
---
# <a name="iaddrbookgetsearchpath"></a>IAddrBook::GetSearchPath

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine geordnete Liste der Eintragsbezeichner der Container zurück, die in den von der [IAddrBook::ResolveName-Methode](iaddrbook-resolvename.md) initiierten Namensauflösungsprozess einbezogen werden sollen. 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der im Suchpfad zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 _lppSearchPath_
  
> [out] Ein Zeiger auf einen Zeiger auf eine geordnete Liste von Containereintragsbezeichnern. **GetSearchPath** speichert die geordnete Liste in einer [SRowSet-Struktur.](srowset.md) Wenn keine Container in der Adressbuchhierarchie enthalten sind, wird null in der **SRowSet-Struktur** zurückgegeben. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Suchpfad wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Hinweise

Clients und Dienstanbieter rufen die **GetSearchPath-Methode** auf, um den Suchpfad zu erhalten, der zum Auflösen von Namen mit der **ResolveName-Methode verwendet** wird. In der Regel rufen Clients die [IAddrBook::SetSearchPath-Methode](iaddrbook-setsearchpath.md) auf, um einen Containersuchpfad im Profil zu erstellen, bevor sie **GetSearchPath** aufrufen, um ihn abzurufen. Das Aufrufen von **SetSearchPath** ist jedoch optional. 
  
Wenn **SetSearchPath** noch nie aufgerufen wurde, erstellt **GetSearchPath** einen Pfad, indem die Hierarchietabellen des Adressbuchs durchforscht werden. Der von **GetSearchPath** festgelegte Standardsuchpfad besteht aus den folgenden Containern in der folgenden Reihenfolge: 
  
1. Der erste Container mit Lese-/Schreibberechtigung, in der Regel das persönliche Adressbuch (PAB).
    
2. Jeder Container, dessen **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) -Eigenschaft auf DT_GLOBAL. Diese Einstellung gibt an, dass der Container Empfänger enthält. 
    
3. Der als Standard festgelegte Container, wenn keine Container mit der DT_GLOBAL-Kennzeichnung in ihrer **PR_DISPLAY_TYPE-Eigenschaft** festgelegt sind und der Standardcontainer sich vom ersten Container mit Lese-/Schreibberechtigung unterscheidet. 
    
Wenn **SetSearchPath** aufgerufen wurde, erstellt **GetSearchPath** einen Pfad mithilfe der Adressbuchcontainer, die im Profil gespeichert wurden. **GetSearchPath** überprüft diesen Pfad, bevor er an den Aufrufer zurückgibt. 
  
Nach dem ersten Aufruf von **SetSearchPath** müssen nachfolgende Aufrufe von **SetSearchPath** verwendet werden, um den von **GetSearchPath** zurückgegebenen Suchpfad zu ändern. Anders ausgedrückt: Der aufrufende Client oder Anbieter erhält nach dem ersten Aufruf von SetSearchPath nicht den **Standardsuchpfad.**
  
## <a name="see-also"></a>Siehe auch



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

