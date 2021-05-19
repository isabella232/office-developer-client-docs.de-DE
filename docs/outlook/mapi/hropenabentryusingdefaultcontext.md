---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f60c4d3761694439d10b073fda5bc36443c13e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434340"
---
# <a name="hropenabentryusingdefaultcontext"></a>HrOpenABEntryUsingDefaultContext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führt dieselbe Funktion wie [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) aus, mit der Ausnahme, dass der ältere **emsmdbUID** als  _pEmsmdbUID-Parameter verwendet_ wird. Verwenden Sie diese Funktion nur, wenn Sie die richtige **emsmdbUID** für den Aufruf von [HrOpenABEntryWithExchangeContext nicht abrufen können.](hropenabentrywithexchangecontext.md)
  
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
  
> [in] Die angemeldete **IMAPISession**. Es kann nicht NULL sein.
    
 _pAddrBook_
  
> [in] Das Adressbuch, das zum Öffnen der Eintrags-ID verwendet wird. Es kann nicht NULL sein.
    
 _cbEntryID_
  
> [in] Die Byteanzahl des Eintragsbezeichners, der durch den  _lpEntryID-Parameter angegeben_ wird. 
    
 _lpEntryID_
  
>  [in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnende Adressbucheintrag darstellt. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet wird. Durch Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben. Für Messagingbenutzer ist die Standardschnittstelle [IMailUser : IMAPIProp](imailuserimapiprop.md). Für Verteilerlisten ist [IDistList : IMAPIContainer](idistlistimapicontainer.md)und für Container [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Anrufer können  _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Eintrag geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_BEST_ACCESS
  
> Fordert an, dass der Eintrag mit den maximal zulässigen Netzwerk- und Clientberechtigungen geöffnet wird. Wenn der Client beispielsweise über Lese- und Schreibberechtigungen verfügt, versucht der Adressbuchanbieter, den Eintrag mit Lese- und Schreibberechtigung zu öffnen. Der Client kann die Zugriffsebene abrufen, die gewährt wurde, indem die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des geöffneten Eintrags aufgerufen und die PR_ACCESS_LEVEL -Eigenschaft (PidTagAccessLevel) abgerufen wird. 
    
MAPI_CACHE_ONLY
  
> Verwendet nur das Offlineadressbuch, um die Namensauflösung durchzuführen. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung zu ermöglichen, die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und aus dem Cache auf einen Eintrag in diesem Adressbuch zu zugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Adressbuchanbieter Exchange unterstützt.
    
MAPI_DEFERRED_ERRORS
  
> Ermöglicht den Erfolgreichen Aufruf, möglicherweise bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass nachfolgende Aufrufe des Eintrags möglicherweise einen Fehler zurückgeben.
    
MAPI_GAL_ONLY
  
> Verwendet nur die GAL, um die Namensauflösung durchzuführen. Dieses Flag wird nur vom Adressbuchanbieter Exchange unterstützt.
    
MAPI_MODIFY
  
> Fordert an, dass der Eintrag mit Lese- und Schreibberechtigung geöffnet wird. Da Einträge standardmäßig mit schreibgeschützten Zugriffen geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese- und Schreibberechtigungen gewährt wurden, unabhängig davon, ob MAPI_MODIFY festgelegt ist.
    
MAPI_NO_CACHE
  
> Verwendet das Offlineadressbuch nicht zum Ausführen der Namensauflösung. Dieses Flag wird nur vom Adressbuchanbieter Exchange unterstützt.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Eintrags.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger des geöffneten Eintrags.
    

