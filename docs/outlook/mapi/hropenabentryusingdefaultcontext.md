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
  
Führt die gleiche Funktion wie [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) aus, außer dass der Legacy- **emsmdbUID** als _pEmsmdbUID_ -Parameter verwendet wird. Verwenden Sie diese Funktion nur, wenn Sie nicht die richtige **emsmdbUID** für den Aufruf von [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)abrufen können.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> in Der angemeldete **IMAPISession**. Er darf nicht NULL sein.
    
 _pAddrBook_
  
> in Das zum Öffnen des Eintrags Bezeichners verwendete Adressbuch. Er darf nicht NULL sein.
    
 _cbEntryID_
  
> in Die Bytezahl der vom _lpEntryID_ -Parameter angegebenen Eintrags-ID. 
    
 _lpEntryID_
  
>  in Ein Zeiger auf die Eintrags-ID, die den zu öffnenden Adressbucheintrag darstellt. 
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet wird. Beim Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben. Für Messagingbenutzer ist die Standardschnittstelle [IMailUser: IMAPIProp](imailuserimapiprop.md). Für Verteilerlisten ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md), und für Container ist es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Anrufer können _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen. 
    
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
    
 _lpulObjType_
  
> Out Ein Zeiger auf den Typ des geöffneten Eintrags.
    
 _lppUnk_
  
> Out Ein Zeiger auf einen Zeiger des geöffneten Eintrags.
    

