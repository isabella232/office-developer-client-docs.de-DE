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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
_lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID, die den zu öffnenden Adressbucheintrag darstellt.
    
_lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet werden soll. Durch das Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben. Für Messagingbenutzer ist die Standardschnittstelle [IMailUser: IMAPIProp](imailuserimapiprop.md). Für Verteilerlisten ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md) und für Container ist es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Anrufer können _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen. 
    
_ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie der Eintrag geöffnet wird. Die folgenden Flags können festgelegt werden.
    
MAPI_BEST_ACCESS 
  
> Fordert, dass der Eintrag mit den maximal zulässigen Netzwerk-und Clientberechtigungen geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, sollte der Adressbuchanbieter versuchen, den Eintrag mit Berechtigung zum Lesen/Schreiben zu öffnen. Der Client kann die Zugriffsebene abrufen, die durch Aufrufen der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Open-Eintrags und Abrufen der **PR_ACCESS_LEVEL** ([pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))-Eigenschaft erteilt wurde.
    
MAPI_CACHE_ONLY
  
> Öffnet einen Adressbucheintrag und greift nur über den Cache auf ihn zu. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    
MAPI_DEFERRED_ERRORS 
  
> Der Aufruf kann erfolgreich ausgeführt werden, bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass spätere Aufrufe des Eintrags möglicherweise einen Fehler zurückgeben.
    
MAPI_GAL_ONLY
  
> Verwenden Sie nur die GAL zum Durchführen der Namensauflösung. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    
  > [!NOTE]
  > Der _ulFlags_ -MAPI_GAL_ONLY ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben, in diesem Fall können Sie ihn mithilfe des folgenden Werts zu Ihrem Code hinzufügen: >`#define MAPI_GAL_ONLY (0x00000080)`
  
MAPI_MODIFY 
  
> Fordert, dass der Eintrag mit Lese-/Schreibzugriff geöffnet wird. Da Einträge standardmäßig mit schreibgeschütztem Zugriff geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese-/Schreibzugriff erteilt wurde, unabhängig davon, ob MAPI_MODIFY festgelegt ist.
    
MAPI_NO_CACHE
  
> Verwenden Sie das Offlineadressbuch nicht zum Ausführen der Namensauflösung. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    
_lpulObjType_
  
> Out Ein Zeiger auf den Typ des geöffneten Eintrags.
    
_lppUnk_
  
> Out Ein Zeiger auf einen Zeiger auf den geöffneten Eintrag.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Eintrag wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, einen Eintrag zu öffnen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der durch _lpEntryID_ dargestellte Eintrag ist nicht vorhanden. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die in _lpEntryID_ angegebene Eintrags-ID wird nicht erkannt. Dieser Wert wird in der Regel zurückgegeben, wenn der für den entsprechenden Eintrag zuständige Adressbuchanbieter nicht geöffnet ist. 
    
## <a name="remarks"></a>Bemerkungen

Clients und Dienstanbieter rufen die **IAddrBook:: OpenEntry** -Methode auf, um einen Adressbucheintrag zu öffnen. MAPI leitet den Anruf an den entsprechenden Adressbuchanbieter weiter, basierend auf der [MAPIUID](mapiuid.md) -Struktur, die in der im _lpEntryID_ -Parameter übergebenen Eintrags-ID enthalten ist. Der Adressbuchanbieter öffnet den Eintrag schreibgeschützt, es sei denn, das MAPI_MODIFY-oder MAPI_BEST_ACCESS-Flag im _ulFlags_ -Parameter ist festgelegt. Diese Flags sind jedoch Vorschläge. Wenn der Adressbuchanbieter die Änderung für den angeforderten Eintrag nicht zulässt, wird MAPI_E_NO_ACCESS zurückgegeben. 
  
Der Parameter _lpInterface_ gibt an, welche Schnittstelle für den Zugriff auf den geöffneten Eintrag verwendet werden soll. Durch das Übergeben von NULL in _lpInterface_ wird angegeben, dass die standardmäßige MAPI-Schnittstelle für diesen Eintragstyp verwendet werden soll. Da der Adressbuchanbieter eine andere Schnittstelle als die vom _lpInterface_ -Parameter vorgeschlagene zurückgeben kann, sollte der Aufrufer den im _lpulObjType_ -Parameter zurückgegebenen Wert überprüfen, um zu bestimmen, ob der zurückgegebene Objekttyp erwartete. Wenn der Objekttyp nicht vom erwarteten Typ ist, kann der Aufrufer den Parameter _lppUnk_ in einen geeigneten Typ umwandeln. 
  
## <a name="see-also"></a>Siehe auch

- [IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

