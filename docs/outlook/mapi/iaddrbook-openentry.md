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
ms.openlocfilehash: fa279962043f6f7cb7a134b624000c9c7e65369f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19792017"
---
# <a name="iaddrbookopenentry"></a>IAddrBook::OpenEntry

**Betrifft**: Outlook 
  
Öffnet ein Adressbuch Adresseintrag, und gibt einen Zeiger auf eine Schnittstelle, die den Eintrag Zugriff auf verwendet werden kann.
  
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
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
_lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt.
    
_lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID) der Schnittstelle, greifen Sie auf den Eintrag open verwendet werden soll. Übergeben von NULL gibt Standardschnittstelle für das Objekt zurück. Für die messaging-Benutzer ist der standard-Benutzeroberfläche [IMailUser: IMAPIProp](imailuserimapiprop.md). Verteilerlisten, ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md) und Containern, ist es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Anrufer können auf die entsprechende standard-Schnittstelle oder eine Schnittstelle in der Vererbungshierarchie _LpInterface_ festlegen. 
    
_ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie der Eintrag geöffnet wird. Die folgenden Kennzeichen können festgelegt werden.
    
MAPI_BEST_ACCESS 
  
> Fordert, dass der Eintrag mit den maximalen zulässigen Netzwerk- und Client Berechtigungen geöffnet werden. Wenn der Client über Lese-/Schreibberechtigung verfügt, sollten beispielsweise die Adressbuchanbieter versuchen, um den Eintrag mit Lese-/Schreibzugriff zu öffnen. Der Client kann die Zugriffsebene abzurufen, die durch Aufrufen der open Eintrag [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode und Abrufen der Eigenschaft **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) gewährt wurde.
    
MAPI_CACHE_ONLY
  
> Öffnet ein Adressbuch Adresseintrag und greift er nur aus dem Cache. Dieses Kennzeichen können Sie beispielsweise ermöglichen einer Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht den Anruf, potenziell erfolgreich ausgeführt werden kann, bevor der Eintrag vollständig geöffnet und kann, sagen, dass später aufruft, um den Eintrag einen Fehler zurück, möglicherweise ist.
    
MAPI_GAL_ONLY
  
> Verwenden Sie nur die globale Adressliste, um namensauflösung auszuführen. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
  > [!NOTE]
  > _UlFlags_ MAPI_GAL_ONLY möglicherweise nicht in der herunterladbaren Headerdatei derzeit definiert werden, in diesem Fall können Sie es dem Code mit dem folgenden Wert hinzufügen: >`#define MAPI_GAL_ONLY (0x00000080)`
  
MAPI_MODIFY 
  
> Anforderungen, denen der Eintrag geöffnet werden, mit Lese-/Schreibberechtigung. Da Einträge standardmäßig mit schreibgeschützten Zugriff geöffnet sind, sollte Clients nicht wird vorausgesetzt, dass Lese-/Schreibberechtigung erteilt wurde, unabhängig davon, ob MAPI_MODIFY festgelegt ist.
    
MAPI_NO_CACHE
  
> Verwenden Sie das Offlineadressbuch nicht namensauflösung ausführen. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
_lpulObjType_
  
> [out] Ein Zeiger auf den Typ des Eintrags geöffnet.
    
_lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf den Eintrag geöffnet.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Eintrag wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, einen Eintrag zu öffnen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der Eintrag durch _LpEntryID_ dargestellt ist nicht vorhanden. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die in _LpEntryID_ angegebene Eintrags-ID wird nicht erkannt. Dieser Wert wird in der Regel zurückgegeben, wenn die Adressbuchanbieter verantwortlich für den entsprechenden Eintrag nicht geöffnet ist. 
    
## <a name="remarks"></a>Hinweise

Clients und -Dienstanbieter rufen Sie die **IAddrBook::OpenEntry** -Methode, um ein Adressbuch Adresseintrag zu öffnen. MAPI leitet den Anruf an die entsprechenden Adressbuchanbieter basierend auf der [MAPIUID](mapiuid.md) -Struktur in die Eintrags-ID in der _LpEntryID_ -Parameter übergeben enthalten. Der Adressbuchanbieter öffnet den Eintrag im schreibgeschützten Modus, es sei denn, das Flag MAPI_MODIFY oder MAPI_BEST_ACCESS im _UlFlags_ -Parameter festgelegt ist. Allerdings werden diese Flags Vorschläge. Wenn die Adressbuchanbieter keine Änderung für den Eintrag angefordert zulässt, wird MAPI_E_NO_ACCESS zurückgegeben. 
  
Der Parameter _LpInterface_ gibt an, welche Schnittstelle zum Zugriff auf die geöffnete Eintrag verwendet werden soll. Übergeben von NULL in _LpInterface_ gibt an, dass die standard-MAPI-Schnittstelle für diesen Eintrag verwendet werden soll. Da die Adressbuchanbieter eine andere Schnittstelle als die durch den Parameter _LpInterface_ vorgeschlagene zurückgegeben werden, sollte der Aufrufer überprüfen Sie den Wert zurückgegeben, die in der _LpulObjType_ -Parameter, um festzustellen, ob der Objekttyp zurückgegeben wird Was wurde erwartet. Wenn der Objekttyp nicht mit dem erwarteten Typ ist, kann der Aufrufer den _LppUnk_ -Parameter auf einen Typ umgewandelt, die besser geeignet ist. 
  
## <a name="see-also"></a>Siehe auch

- [IAddrBook: IMAPIProp](iaddrbookimapiprop.md)

