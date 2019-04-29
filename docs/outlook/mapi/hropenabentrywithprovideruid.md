---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 20344185ffcbd90017fa3c3493218bd9b3ddfd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408894"
---
# <a name="hropenabentrywithprovideruid"></a>HrOpenABEntryWithProviderUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet die **Eintrags** -Nr. mit dem von _PEmsabpUID_identifizierten Exchange-Adressbuch. Diese Funktion funktioniert ähnlich wie [IAddrBook:: OpenEntry](iaddrbook-openentry.md) , mit der Ausnahme, dass mit dieser Funktion sichergestellt wird, dass [IAddrBook:: OpenEntry](iaddrbook-openentry.md) unter Verwendung des erwarteten Exchange-Adressbuch Anbieters geöffnet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> in Ein Zeiger auf ein **emsmdbUID** , das den Exchange-Dienst identifiziert, der den Exchange-Adressbuchanbieter enthält, den diese Funktion verwenden sollte, um Details zur Eintrags-ID anzuzeigen. Wenn die ID des eingehenden Eintrags kein Exchange-Adressbuchanbieter ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::D ails](iaddrbook-details.md). Wenn dieser Parameter NULL oder eine NULL-MAPIUID ist, verhält sich diese Funktion wie [IAddrBook::D ails](iaddrbook-details.md).
    
 _pAddrBook_
  
> in Das zum Öffnen des Eintrags Bezeichners verwendete Adressbuch. Er darf nicht NULL sein.
    
 _cbEntryID_
  
> in Die Bytezahl der vom _lpEntryID_ -Parameter angegebenen Eintrags-ID. 
    
 _lpEntryID_
  
>  in Ein Zeiger auf die Eintrags-ID, die den zu öffnenden Adressbucheintrag darstellt. 
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet wird. Beim Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben. Für Messagingbenutzer ist die Standardschnittstelle [IMailUser: IMAPIProp](imailuserimapiprop.md). Für Verteilerlisten ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md)und für Container ist es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Anrufer können _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die das Öffnen des Eintrags steuert, können die folgenden Flags festgelegt werden:
    
MAPI_BEST_ACCESS
  
> Fordert, dass der Eintrag mit den maximal zulässigen Netzwerk-und Clientberechtigungen geöffnet wird. Wenn der Client beispielsweise über Lese-und Schreibberechtigungen verfügt, versucht der Adressbuchanbieter, den Eintrag mit Lese-und Schreibberechtigung zu öffnen. Der Client kann die Zugriffsebene abrufen, die durch Aufrufen der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des geöffneten Eintrags und Abrufen der PR_ACCESS_LEVEL (pidtagaccesslevel ()-Eigenschaft erteilt wurde. 
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    
MAPI_DEFERRED_ERRORS
  
> Der Aufruf kann erfolgreich ausgeführt werden, bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass nachfolgende Aufrufe des Eintrags möglicherweise einen Fehler zurückgeben.
    
MAPI_GAL_ONLY
  
> Verwenden Sie nur die GAL zum Durchführen der Namensauflösung. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    
MAPI_MODIFY
  
> Fordert, dass der Eintrag mit Lese-und Schreibberechtigung geöffnet wird. Da Einträge standardmäßig mit schreibgeschütztem Zugriff geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese-und Schreibberechtigungen erteilt wurden, unabhängig davon, ob MAPI_MODIFY festgelegt ist.
    
MAPI_NO_CACHE
  
> Verwenden Sie das Offlineadressbuch nicht zum Ausführen der Namensauflösung. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    
 _lpulObjType_
  
> Out Ein Zeiger auf den Typ des geöffneten Eintrags.
    
 _lppUnk_
  
> Out Ein Zeiger auf einen Zeiger des geöffneten Eintrags.
    

