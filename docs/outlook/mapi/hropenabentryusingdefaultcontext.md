---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 74660de551d43c589cb903b5c3852136f2f18269
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791930"
---
# <a name="hropenabentryusingdefaultcontext"></a>HrOpenABEntryUsingDefaultContext

  
  
**Betrifft**: Outlook 
  
Führt die gleiche Funktion wie [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , mit der Ausnahme, dass es der Vorgängerversion **EmsmdbUID** als _pEmsmdbUID_ -Parameter verwendet. Verwenden Sie diese Funktion nicht, es sei denn, Sie nicht die richtige **EmsmdbUID** für den Aufruf von [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)beziehen können.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
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
  
> [in] Die angemeldete **IMAPISession**. Es darf nicht NULL sein.
    
 _pAddrBook_
  
> [in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen. Es darf nicht NULL sein.
    
 _cbEntryID_
  
> [in] Die Byteanzahl des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben. 
    
 _lpEntryID_
  
>  [in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID) der Schnittstelle, die den Eintrag open Zugriff auf verwendet wird. Übergeben von NULL gibt die standard-Schnittstelle des Objekts zurück. Für die messaging-Benutzer ist der standard-Benutzeroberfläche [IMailUser: IMAPIProp](imailuserimapiprop.md). Wird für es Verteilerlisten [IDistList: IMAPIContainer](idistlistimapicontainer.md), und für Container ist [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Anrufer können auf die entsprechende standard-Schnittstelle oder eine Schnittstelle in der Vererbungshierarchie _LpInterface_ festlegen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie der Eintrag geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_BEST_ACCESS
  
> Fordert, dass der Eintrag mit den maximalen zulässigen Netzwerk- und Client Berechtigungen geöffnet werden. Wenn der Client über Lese- und Schreibberechtigungen, versucht der Adressbuchanbieter beispielsweise, öffnen Sie den Eintrag mit Lese- und Schreibberechtigungen. Der Client kann die Zugriffsebene abzurufen, die durch Aufrufen der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode des Eintrags öffnen und das Abrufen der Eigenschaft PR_ACCESS_LEVEL (PidTagAccessLevel) gewährt wurde. 
    
MAPI_CACHE_ONLY
  
> Verwendet nur das Offlineadressbuch namensauflösung ausführen. Dieses Kennzeichen können Sie beispielsweise ermöglichen einer Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
MAPI_DEFERRED_ERRORS
  
> Ermöglicht den Anruf, potenziell erfolgreich ausgeführt werden kann, bevor der Eintrag vollständig geöffnet und verfügbar ist, dass dies, dass nachfolgende Aufrufe von den Eintrag möglicherweise einen Fehler zurück, ist.
    
MAPI_GAL_ONLY
  
> Verwendet nur die globale Adressliste namensauflösung ausführen. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
MAPI_MODIFY
  
> Anforderungen, denen mit der Eintrag geöffnet werden Lese- und Schreibberechtigungen. Da die Einträge in der Standardeinstellung mit schreibgeschützten Zugriff geöffnet sind, sollte Clients nicht davon ausgehen, das Lesen und schreiben, dass die Berechtigung erteilt wurde, unabhängig davon, ob MAPI_MODIFY festgelegt ist.
    
MAPI_NO_CACHE
  
> Das Offlineadressbuch wird nicht zum Ausführen von namensauflösung verwendet werden. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des Eintrags geöffnet.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger des Eintrags geöffnet.
    

