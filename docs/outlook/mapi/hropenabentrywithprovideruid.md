---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: efea46940881750c0c35765e1a3074a03d3fed81
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571955"
---
# <a name="hropenabentrywithprovideruid"></a>HrOpenABEntryWithProviderUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet die **entryID** mithilfe des Exchange Adressbuchs, das durch _pEmsabpUID_ identifiziert wird. Diese Funktion funktioniert ähnlich wie [IAddrBook::OpenEntry,](iaddrbook-openentry.md) mit der Ausnahme, dass die Verwendung dieser Funktion sicherstellt, dass [IAddrBook::OpenEntry](iaddrbook-openentry.md) mithilfe des erwarteten Exchange Adressbuchanbieters geöffnet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
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
  
> [in] Ein Zeiger auf eine **emsmdbUID,** die den Exchange Dienst identifiziert, der den Exchange Adressbuchanbieter enthält, den diese Funktion verwenden soll, um Details zum Eintragsbezeichner anzuzeigen. Wenn der Bezeichner für den eingehenden Eintrag kein Exchange Adressbuchanbieter-Eintragsbezeichner ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::D etails](iaddrbook-details.md). Wenn dieser Parameter NULL oder eine Null MAPIUID ist, verhält sich diese Funktion wie [IAddrBook::D etails](iaddrbook-details.md).
    
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
  
> Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung auszuführen. Beispielsweise können Sie dieses Flag verwenden, um einer Clientanwendung das Öffnen der globalen Adressliste (GAL) im Cache-Exchange-Modus und den Zugriff auf einen Eintrag in diesem Adressbuch aus dem Cache zu ermöglichen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
MAPI_DEFERRED_ERRORS
  
> Ermöglicht, dass der Aufruf erfolgreich ist, möglicherweise bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass nachfolgende Aufrufe des Eintrags einen Fehler zurückgeben können.
    
MAPI_GAL_ONLY
  
> Verwenden Sie nur die GAL, um die Namensauflösung auszuführen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
MAPI_MODIFY
  
> Fordert an, dass der Eintrag mit Lese- und Schreibberechtigung geöffnet wird. Da Einträge standardmäßig mit schreibgeschütztem Zugriff geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese- und Schreibberechtigungen erteilt wurden, unabhängig davon, ob MAPI_MODIFY festgelegt ist.
    
MAPI_NO_CACHE
  
> Verwenden Sie das Offlineadressbuch nicht, um die Namensauflösung auszuführen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Eintrags.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger des geöffneten Eintrags.
    

