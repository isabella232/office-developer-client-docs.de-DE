---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8dac41f54e1510e69ec776cc2b4d7938b728321b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561621"
---
# <a name="hropenabentrywithexchangecontext"></a>HrOpenABEntryWithExchangeContext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet die **entryID** mithilfe des von **pEmsmdbUID identifizierten Exchange Adressbuchs.** Diese Funktion funktioniert ähnlich wie [IAddrBook::D Etails,](iaddrbook-details.md) mit der Ausnahme, dass die Verwendung dieser Funktion sicherstellt, dass das [IAddrBook::OpenEntry](iaddrbook-openentry.md) mithilfe des erwarteten Exchange Adressbuchanbieters geöffnet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
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
  
> [in] Die angemeldete **IMAPISession**. Er darf nicht NULL sein.
    
 _pEmsmdbUID_
  
> [in] Ein Zeiger auf eine **emsmdbUID,** die den Exchange Dienst identifiziert, der den Exchange Adressbuchanbieter enthält, den diese Funktion verwenden soll, um Details zum Eintragsbezeichner anzuzeigen. Wenn der Bezeichner für den eingehenden Eintrag kein Exchange Adressbuchanbieter-Eintragsbezeichner ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::D etails](iaddrbook-details.md). Wenn dieser Parameter NULL oder eine Null MAPIUID ist, verhält sich diese Funktion wie [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] Das Zum Öffnen des Eintragsbezeichners verwendete Adressbuch. Er darf nicht NULL sein.
    
 _cbEntryID_
  
> [in] Die Byteanzahl des Eintragsbezeichners, der durch den  _lpEntryID-Parameter_ angegeben wird. 
    
 _lpEntryID_
  
>  [in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnenden Adressbucheintrag darstellt. 
    
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
    

