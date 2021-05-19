---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: 'Letzte �nderung: Freitag, 1. Februar 2013'
ms.openlocfilehash: 293fe5a65c760f61ab0073e0eafc1a606c69050f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434165"
---
# <a name="iaddrbookopenentry"></a>IAddrBook::OpenEntry

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Adressbucheintrag und gibt einen Zeiger auf eine Schnittstelle zurück, die für den Zugriff auf den Eintrag verwendet werden kann.
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameter

_cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
_lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnende Adressbucheintrag darstellt.
    
_lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet werden soll. Durch Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben. Für Messagingbenutzer ist die Standardschnittstelle [IMailUser : IMAPIProp](imailuserimapiprop.md). Für Verteilerlisten ist [IDistList : IMAPIContainer](idistlistimapicontainer.md) und für Container [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Anrufer können  _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen. 
    
_ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Eintrag geöffnet wird. Die folgenden Flags können festgelegt werden.
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass der Eintrag mit den maximal zulässigen Netzwerk- und Clientberechtigungen geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte der Adressbuchanbieter versuchen, den Eintrag mit Lese-/Schreibberechtigung zu öffnen. Der Client kann die Zugriffsebene abrufen, die gewährt wurde, indem die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des geöffneten Eintrags aufgerufen und die **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) -Eigenschaft abgerufen wird.
    
MAPI_CACHE_ONLY
  
> Öffnet einen Adressbucheintrag und zugrifft ihn nur aus dem Cache. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung zu ermöglichen, die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und aus dem Cache auf einen Eintrag in diesem Adressbuch zu zugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Adressbuchanbieter Exchange unterstützt.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht den Erfolgreichen Aufruf, möglicherweise bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass spätere Aufrufe des Eintrags möglicherweise einen Fehler zurückgeben.
    
MAPI_GAL_ONLY
  
> Verwenden Sie nur die GAL, um die Namensauflösung durchzuführen. Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.
    
  > [!NOTE]
  > Die  _ulFlags MAPI_GAL_ONLY-Datei_ ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie sie ihrem Code mit dem folgenden Wert hinzufügen: >  `#define MAPI_GAL_ONLY (0x00000080)`
  
MAPI_MODIFY 
  
> Fordert an, dass der Eintrag mit Lese-/Schreibberechtigung geöffnet wird. Da Einträge standardmäßig mit schreibgeschützten Zugriffen geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese-/Schreibberechtigungen gewährt wurden, unabhängig davon, ob MAPI_MODIFY festgelegt ist.
    
MAPI_NO_CACHE
  
> Verwenden Sie das Offlineadressbuch nicht, um die Namensauflösung durchzuführen. Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.
    
_lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Eintrags.
    
_lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf den geöffneten Eintrag.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Eintrag wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, einen Eintrag zu öffnen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der durch  _lpEntryID dargestellte_ Eintrag ist nicht vorhanden. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der in  _lpEntryID angegebene_ Eintragsbezeichner wird nicht erkannt. Dieser Wert wird in der Regel zurückgegeben, wenn der adressbuchanbieter, der für den entsprechenden Eintrag verantwortlich ist, nicht geöffnet ist. 
    
## <a name="remarks"></a>Hinweise

Clients und Dienstanbieter rufen die **IAddrBook::OpenEntry-Methode** auf, um einen Adressbucheintrag zu öffnen. MAPI gibt den Aufruf an den entsprechenden Adressbuchanbieter weiter, basierend auf der [MAPIUID-Struktur,](mapiuid.md) die im Eintragsbezeichner enthalten ist, der im  _lpEntryID-Parameter übergeben_ wird. Der Adressbuchanbieter öffnet den Eintrag als schreibgeschützt, es sei denn, MAPI_MODIFY oder MAPI_BEST_ACCESS im  _ulFlags-Parameter_ festgelegt ist. Diese Kennzeichen sind jedoch Vorschläge. Wenn der Adressbuchanbieter keine Änderung für den angeforderten Eintrag zugibt, gibt er MAPI_E_NO_ACCESS. 
  
Der  _lpInterface-Parameter_ gibt an, welche Schnittstelle für den Zugriff auf den geöffneten Eintrag verwendet werden soll. Das Übergeben von NULL in  _lpInterface_ gibt an, dass die standardmäßige MAPI-Schnittstelle für diesen Eintragstyp verwendet werden soll. Da der Adressbuchanbieter möglicherweise eine andere Schnittstelle zurücksenkt als die vom  _lpInterface-Parameter_ vorgeschlagene, sollte der Aufrufer den im  _lpulObjType-Parameter_ zurückgegebenen Wert überprüfen, um festzustellen, ob der zurückgegebene Objekttyp den erwarteten Wert hat. Wenn der Objekttyp nicht den erwarteten Typ hat, kann der Aufrufer den  _lppUnk-Parameter_ in einen geeigneteren Typ umbetten. 
  
## <a name="see-also"></a>Siehe auch

- [IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

