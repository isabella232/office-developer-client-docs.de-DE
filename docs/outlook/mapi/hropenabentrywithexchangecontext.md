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
ms.openlocfilehash: 415d108f7fd9e84ba2a9090658bc0923550390f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347789"
---
# <a name="hropenabentrywithexchangecontext"></a>HrOpenABEntryWithExchangeContext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet die **Eintrags** -Nr. mit dem von **PEmsmdbUID**identifizierten Exchange-Adressbuch. Diese Funktion funktioniert ähnlich wie [IAddrBook::D ails](iaddrbook-details.md) , mit der Ausnahme, dass mit dieser Funktion sichergestellt wird, dass der [IAddrBook:: OpenEntry](iaddrbook-openentry.md) mithilfe des erwarteten Exchange-Adressbuch Anbieters geöffnet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> in Der angemeldete **IMAPISession**. Er darf nicht NULL sein.
    
 _pEmsmdbUID_
  
> in Ein Zeiger auf ein **emsmdbUID** , das den Exchange-Dienst identifiziert, der den Exchange-Adressbuchanbieter enthält, den diese Funktion verwenden sollte, um Details zur Eintrags-ID anzuzeigen. Wenn die ID des eingehenden Eintrags kein Exchange-Adressbuchanbieter ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::D ails](iaddrbook-details.md). Wenn dieser Parameter NULL oder eine NULL-MAPIUID ist, verhält sich diese Funktion wie [IAddrBook::D ails](iaddrbook-details.md).
    
 _pAddrBook_
  
> in Das zum Öffnen des Eintrags Bezeichners verwendete Adressbuch. Er darf nicht NULL sein.
    
 _cbEntryID_
  
> in Die Bytezahl der vom _lpEntryID_ -Parameter angegebenen Eintrags-ID. 
    
 _lpEntryID_
  
>  in Ein Zeiger auf die Eintrags-ID, die den zu öffnenden Adressbucheintrag darstellt. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie der Eintrag geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_BEST_ACCESS
  
> Fordert, dass der Eintrag mit den maximal zulässigen Netzwerk-und Clientberechtigungen geöffnet wird. Wenn der Client beispielsweise über Lese-und Schreibberechtigungen verfügt, versucht der Adressbuchanbieter, den Eintrag mit Lese-und Schreibberechtigung zu öffnen. Der Client kann die Zugriffsebene abrufen, die durch Aufrufen der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des geöffneten Eintrags und Abrufen der PR_ACCESS_LEVEL (pidtagaccesslevel ()-Eigenschaft erteilt wurde. 
    
MAPI_CACHE_ONLY
  
> Verwendet nur das Offlineadressbuch zum Durchführen der Namensauflösung. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    
MAPI_DEFERRED_ERRORS
  
> Der Aufruf kann erfolgreich ausgeführt werden, bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass nachfolgende Aufrufe des Eintrags möglicherweise einen Fehler zurückgeben.
    
MAPI_GAL_ONLY
  
> Verwendet nur die GAL zur Namensauflösung. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    
MAPI_MODIFY
  
> Fordert, dass der Eintrag mit Lese-und Schreibberechtigung geöffnet wird. Da Einträge standardmäßig mit schreibgeschütztem Zugriff geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese-und Schreibberechtigungen erteilt wurden, unabhängig davon, ob MAPI_MODIFY festgelegt ist.
    
MAPI_NO_CACHE
  
> Das Offlineadressbuch wird nicht zum Durchführen der Namensauflösung verwendet. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    

