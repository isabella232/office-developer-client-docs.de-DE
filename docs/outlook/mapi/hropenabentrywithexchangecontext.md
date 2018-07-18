---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fcedaf689db8280b4649662ba61c8468d0f98305
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791929"
---
# <a name="hropenabentrywithexchangecontext"></a>HrOpenABEntryWithExchangeContext

  
  
**Betrifft**: Outlook 
  
Öffnet die **Eintrags-ID** mithilfe der Exchange-Adressbuch durch **pEmsmdbUID**identifiziert. Diese Funktion arbeitet ähnlich wie [IAddrBook::Details](iaddrbook-details.md) mit der Ausnahme, dass mit dieser Funktion wird sichergestellt, dass die [IAddrBook::OpenEntry](iaddrbook-openentry.md) mithilfe der erwarteten Exchange-Adressbuchanbieter geöffnet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _pmsess_
  
> [in] Die angemeldete **IMAPISession**. Es darf nicht NULL sein.
    
 _pEmsmdbUID_
  
> [in] Ein Zeiger auf eine **EmsmdbUID** , die den Exchange-Dienst identifiziert, die die Exchange-Adressbuchanbieter enthält, die diese Funktion zum Anzeigen von Details auf die Eintrags-ID verwendet werden soll. Wenn eingehende Eintrags-ID nicht um ein Exchange-Adressbuchanbieter Eintrags-ID ist, dieser Parameter wird ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::Details](iaddrbook-details.md). Wenn dieser Parameter auf NULL oder eine MAPIUID NULL ist, verhält sich diese Funktion wie [IAddrBook::Details](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen. Es darf nicht NULL sein.
    
 _cbEntryID_
  
> [in] Die Byteanzahl des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben. 
    
 _lpEntryID_
  
>  [in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt. 
    
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
    

