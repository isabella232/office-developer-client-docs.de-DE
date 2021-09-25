---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c64d1390068ac76771556fa0cbc47b8e7c64cdde
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561628"
---
# <a name="hropenabentryusingdefaultcontext"></a>HrOpenABEntryUsingDefaultContext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führt dieselbe Funktion wie [HrOpenABEntryWithExchangeContext aus,](hropenabentrywithexchangecontext.md) mit der Ausnahme, dass die ältere **EmsmdbUID** als _pEmsmdbUID-Parameter verwendet wird._ Verwenden Sie diese Funktion nur, wenn Sie die richtige **emsmdbUID** für den Aufruf von [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)nicht abrufen können.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
HRESULT HrOpenABEntryUsingDefaultContext(
  LPMAPISESSION pmsess,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameter

 _pmsess_
  
> [in] Die angemeldete **IMAPISession**. Er darf nicht NULL sein.
    
 _pAddrBook_
  
> [in] Das Zum Öffnen des Eintragsbezeichners verwendete Adressbuch. Er darf nicht NULL sein.
    
 _cbEntryID_
  
> [in] Die Byteanzahl des Eintragsbezeichners, der durch den  _lpEntryID-Parameter_ angegeben wird. 
    
 _lpEntryID_
  
>  [in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnenden Adressbucheintrag darstellt. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID) der Schnittstelle, der für den Zugriff auf den geöffneten Eintrag verwendet wird. Wenn NULL übergeben wird, wird die Standardschnittstelle des Objekts zurückgegeben. Für Messaging-Benutzer ist die Standardschnittstelle [IMailUser : IMAPIProp](imailuserimapiprop.md). Für Verteilerlisten ist dies [IDistList : IMAPIContainer](idistlistimapicontainer.md)und für Container [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Aufrufer können  _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Eintrag geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_BEST_ACCESS
  
> Fordert an, dass der Eintrag mit den maximal zulässigen Netzwerk- und Clientberechtigungen geöffnet wird. Wenn der Client beispielsweise über Lese- und Schreibberechtigungen verfügt, versucht der Adressbuchanbieter, den Eintrag mit Lese- und Schreibberechtigung zu öffnen. Der Client kann die Zugriffsebene abrufen, die gewährt wurde, indem er die [IMAPIProp::GetProps-Methode des geöffneten Eintrags](imapiprop-getprops.md) aufruft und die eigenschaft PR_ACCESS_LEVEL (PidTagAccessLevel) abruft. 
    
MAPI_CACHE_ONLY
  
> Verwendet nur das Offlineadressbuch, um die Namensauflösung auszuführen. Beispielsweise können Sie dieses Flag verwenden, um einer Clientanwendung das Öffnen der globalen Adressliste (GAL) im Cache-Exchange-Modus und den Zugriff auf einen Eintrag in diesem Adressbuch aus dem Cache zu ermöglichen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
MAPI_DEFERRED_ERRORS
  
> Ermöglicht, dass der Aufruf erfolgreich ist, möglicherweise bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass nachfolgende Aufrufe des Eintrags einen Fehler zurückgeben können.
    
MAPI_GAL_ONLY
  
> Verwendet nur die GAL, um die Namensauflösung auszuführen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
MAPI_MODIFY
  
> Fordert an, dass der Eintrag mit Lese- und Schreibberechtigung geöffnet wird. Da Einträge standardmäßig mit schreibgeschütztem Zugriff geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese- und Schreibberechtigungen erteilt wurden, unabhängig davon, ob MAPI_MODIFY festgelegt ist.
    
MAPI_NO_CACHE
  
> Verwendet nicht das Offlineadressbuch, um die Namensauflösung auszuführen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Eintrags.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger des geöffneten Eintrags.
    

