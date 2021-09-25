---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: 'Letzte �nderung: Freitag, 1. Februar 2013'
ms.openlocfilehash: b1b6ebd5e7d1ad30e9cc0ef2ad4c706dac6788b5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561572"
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
  
> [in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnenden Adressbucheintrag darstellt.
    
_lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID) der Schnittstelle, der für den Zugriff auf den geöffneten Eintrag verwendet werden soll. Wenn NULL übergeben wird, wird die Standardschnittstelle des Objekts zurückgegeben. Für Messaging-Benutzer ist die Standardschnittstelle [IMailUser : IMAPIProp](imailuserimapiprop.md). Für Verteilerlisten ist dies [IDistList : IMAPIContainer](idistlistimapicontainer.md) und für Container [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Aufrufer können  _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen. 
    
_ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Eintrag geöffnet wird. Die folgenden Flags können festgelegt werden.
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass der Eintrag mit den maximal zulässigen Netzwerk- und Clientberechtigungen geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte der Adressbuchanbieter versuchen, den Eintrag mit Lese-/Schreibberechtigung zu öffnen. Der Client kann die Zugriffsebene abrufen, die gewährt wurde, indem er die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des geöffneten Eintrags aufruft und die **eigenschaft PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) abruft.
    
MAPI_CACHE_ONLY
  
> Öffnet einen Adressbucheintrag und greift nur über den Cache darauf zu. Beispielsweise können Sie dieses Flag verwenden, um einer Clientanwendung das Öffnen der globalen Adressliste (GAL) im Cache-Exchange-Modus und den Zugriff auf einen Eintrag in diesem Adressbuch aus dem Cache zu ermöglichen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht, dass der Aufruf erfolgreich ist, möglicherweise bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass spätere Aufrufe des Eintrags einen Fehler zurückgeben können.
    
MAPI_GAL_ONLY
  
> Verwenden Sie nur die GAL, um die Namensauflösung auszuführen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
  > [!NOTE]
  > Die  _ulFlags-MAPI_GAL_ONLY_ ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie sie Ihrem Code mit dem folgenden Wert hinzufügen: >  `#define MAPI_GAL_ONLY (0x00000080)`
  
MAPI_MODIFY 
  
> Fordert an, dass der Eintrag mit Lese-/Schreibberechtigung geöffnet wird. Da Einträge standardmäßig mit schreibgeschütztem Zugriff geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese-/Schreibberechtigungen erteilt wurden, unabhängig davon, ob MAPI_MODIFY festgelegt ist.
    
MAPI_NO_CACHE
  
> Verwenden Sie das Offlineadressbuch nicht, um die Namensauflösung auszuführen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
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
  
> Der durch  _lpEntryID_ dargestellte Eintrag ist nicht vorhanden. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der in  _lpEntryID_ angegebene Eintragsbezeichner wird nicht erkannt. Dieser Wert wird in der Regel zurückgegeben, wenn der für den entsprechenden Eintrag zuständige Adressbuchanbieter nicht geöffnet ist. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Clients und Dienstanbieter rufen die **IAddrBook::OpenEntry-Methode** auf, um einen Adressbucheintrag zu öffnen. Die MAPI leitet den Aufruf an den entsprechenden Adressbuchanbieter weiter, basierend auf der [MAPIUID-Struktur,](mapiuid.md) die im Eintragsbezeichner enthalten ist, der im  _lpEntryID-Parameter_ übergeben wird. Der Adressbuchanbieter öffnet den Eintrag schreibgeschützt, es sei denn, das flag MAPI_MODIFY oder MAPI_BEST_ACCESS im  _ulFlags-Parameter_ ist festgelegt. Diese Flags sind jedoch Vorschläge. Wenn der Adressbuchanbieter keine Änderung für den angeforderten Eintrag zulässt, wird MAPI_E_NO_ACCESS zurückgegeben. 
  
Der  _LpInterface-Parameter_ gibt an, welche Schnittstelle für den Zugriff auf den geöffneten Eintrag verwendet werden soll. Das Übergeben von NULL in  _lpInterface_ gibt die standardmäßige MAPI-Schnittstelle für diesen Eintragstyp an. Da der Adressbuchanbieter möglicherweise eine andere Schnittstelle als die vom  _lpInterface-Parameter_ vorgeschlagene zurückgibt, sollte der Aufrufer den im  _lpulObjType-Parameter_ zurückgegebenen Wert überprüfen, um zu bestimmen, ob der zurückgegebene Objekttyp dem erwarteten Entspricht. Wenn der Objekttyp nicht dem erwarteten Typ entspricht, kann der Aufrufer den  _lppUnk-Parameter_ in einen besser geeigneten Typ umwandeln. 
  
## <a name="see-also"></a>Siehe auch

- [IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

