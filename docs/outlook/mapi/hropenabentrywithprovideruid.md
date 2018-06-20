---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e33e656e70802437ab8b8717c5e175e2a13e384e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791926"
---
# <a name="hropenabentrywithprovideruid"></a>HrOpenABEntryWithProviderUID

  
  
**Betrifft**: Outlook 
  
Öffnet die **Eintrags-ID** mithilfe der Exchange-Adressbuch durch _pEmsabpUID_identifiziert. Diese Funktion arbeitet ähnlich wie [IAddrBook::OpenEntry](iaddrbook-openentry.md) mit der Ausnahme, dass mit dieser Funktion wird sichergestellt, dass [IAddrBook::OpenEntry](iaddrbook-openentry.md) mit dem erwarteten Exchange-Adressbuch Anbieter geöffnet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUID(
  const MAPIUID *pEmsabpUID,
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

 _pEmsmdbUID_
  
> [in] Ein Zeiger auf eine **EmsmdbUID** , die den Exchange-Dienst identifiziert, die die Exchange-Adressbuchanbieter enthält, die diese Funktion zum Anzeigen von Details auf die Eintrags-ID verwendet werden soll. Wenn eingehende Eintrags-ID nicht um ein Exchange-Adressbuchanbieter Eintrags-ID ist, dieser Parameter wird ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::Details](iaddrbook-details.md). Wenn dieser Parameter auf NULL oder eine MAPIUID NULL ist, verhält sich diese Funktion wie [IAddrBook::Details](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen. Es darf nicht NULL sein.
    
 _cbEntryID_
  
> [in] Die Byteanzahl des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben. 
    
 _lpEntryID_
  
>  [in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID) der Schnittstelle, die den Eintrag open Zugriff auf verwendet wird. Übergeben von NULL gibt die standard-Schnittstelle des Objekts zurück. Für die messaging-Benutzer ist der standard-Benutzeroberfläche [IMailUser: IMAPIProp](imailuserimapiprop.md). Verteilerlisten, ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md)und Containern, ist es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Anrufer können auf die entsprechende standard-Schnittstelle oder eine Schnittstelle in der Vererbungshierarchie _LpInterface_ festlegen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die die wie steuert der Eintrag geöffnet wird, können die folgenden Werte festgelegt werden:
    
MAPI_BEST_ACCESS
  
> Fordert, dass der Eintrag mit den maximalen zulässigen Netzwerk- und Client Berechtigungen geöffnet werden. Wenn der Client über Lese- und Schreibberechtigungen, versucht der Adressbuchanbieter beispielsweise, öffnen Sie den Eintrag mit Lese- und Schreibberechtigungen. Der Client kann die Zugriffsebene abzurufen, die durch Aufrufen der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode des Eintrags öffnen und das Abrufen der Eigenschaft PR_ACCESS_LEVEL (PidTagAccessLevel) gewährt wurde. 
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um namensauflösung auszuführen. Dieses Kennzeichen können Sie beispielsweise ermöglichen einer Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
MAPI_DEFERRED_ERRORS
  
> Ermöglicht den Anruf, potenziell erfolgreich ausgeführt werden kann, bevor der Eintrag vollständig geöffnet und verfügbar ist, dass dies, dass nachfolgende Aufrufe von den Eintrag möglicherweise einen Fehler zurück, ist.
    
MAPI_GAL_ONLY
  
> Verwenden Sie nur die globale Adressliste, um namensauflösung auszuführen. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
MAPI_MODIFY
  
> Anforderungen, denen mit der Eintrag geöffnet werden Lese- und Schreibberechtigungen. Da die Einträge in der Standardeinstellung mit schreibgeschützten Zugriff geöffnet sind, sollte Clients nicht davon ausgehen, das Lesen und schreiben, dass die Berechtigung erteilt wurde, unabhängig davon, ob MAPI_MODIFY festgelegt ist.
    
MAPI_NO_CACHE
  
> Verwenden Sie das Offlineadressbuch nicht namensauflösung ausführen. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des Eintrags geöffnet.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger des Eintrags geöffnet.
    

