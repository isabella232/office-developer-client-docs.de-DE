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
  
Öffnet die **entryID** mit dem Exchange, das von _pEmsabpUID identifiziert wurde._ Diese Funktion funktioniert ähnlich wie [IAddrBook::OpenEntry,](iaddrbook-openentry.md) mit der Ausnahme, dass die Verwendung dieser Funktion sicherstellt, dass [IAddrBook::OpenEntry](iaddrbook-openentry.md) mithilfe des erwarteten Adressbuchanbieters Exchange geöffnet wird. 
  
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
  
> [in] Ein Zeiger auf eine **emsmdbUID,** die den Exchange-Dienst identifiziert, der den Exchange-Adressbuchanbieter enthält, den diese Funktion verwenden soll, um Details zur Eintrags-ID anzuzeigen. Wenn der Bezeichner für eingehende Eingaben kein eintragsbezeichner Exchange Adressbuchanbieter ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::D etails](iaddrbook-details.md). Wenn dieser Parameter NULL oder null MAPIUID ist, verhält sich diese Funktion wie [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] Das Adressbuch, das zum Öffnen der Eintrags-ID verwendet wird. Es kann nicht NULL sein.
    
 _cbEntryID_
  
> [in] Die Byteanzahl des Eintragsbezeichners, der durch den  _lpEntryID-Parameter angegeben_ wird. 
    
 _lpEntryID_
  
>  [in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnende Adressbucheintrag darstellt. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet wird. Durch Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben. Für Messagingbenutzer ist die Standardschnittstelle [IMailUser : IMAPIProp](imailuserimapiprop.md). Für Verteilerlisten ist [IDistList : IMAPIContainer](idistlistimapicontainer.md)und für Container [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Anrufer können  _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske von Flags, die steuert, wie der Eintrag geöffnet wird, Die folgenden Flags können festgelegt werden:
    
MAPI_BEST_ACCESS
  
> Fordert an, dass der Eintrag mit den maximal zulässigen Netzwerk- und Clientberechtigungen geöffnet wird. Wenn der Client beispielsweise über Lese- und Schreibberechtigungen verfügt, versucht der Adressbuchanbieter, den Eintrag mit Lese- und Schreibberechtigung zu öffnen. Der Client kann die Zugriffsebene abrufen, die gewährt wurde, indem die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des geöffneten Eintrags aufgerufen und die PR_ACCESS_LEVEL -Eigenschaft (PidTagAccessLevel) abgerufen wird. 
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung zu ermöglichen, die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und aus dem Cache auf einen Eintrag in diesem Adressbuch zu zugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.
    
MAPI_DEFERRED_ERRORS
  
> Ermöglicht den Erfolgreichen Aufruf, möglicherweise bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass nachfolgende Aufrufe des Eintrags möglicherweise einen Fehler zurückgeben.
    
MAPI_GAL_ONLY
  
> Verwenden Sie nur die GAL, um die Namensauflösung durchzuführen. Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.
    
MAPI_MODIFY
  
> Fordert an, dass der Eintrag mit Lese- und Schreibberechtigung geöffnet wird. Da Einträge standardmäßig mit schreibgeschützten Zugriffen geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese- und Schreibberechtigungen gewährt wurden, unabhängig davon, ob MAPI_MODIFY festgelegt ist.
    
MAPI_NO_CACHE
  
> Verwenden Sie das Offlineadressbuch nicht, um die Namensauflösung durchzuführen. Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Eintrags.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger des geöffneten Eintrags.
    

