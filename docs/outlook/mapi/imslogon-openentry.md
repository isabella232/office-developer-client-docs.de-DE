---
title: IMSLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenEntry
api_type:
- COM
ms.assetid: 612cbab7-60cb-48bb-906e-18d9135e7a86
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 544aaaace18a9d26972e6484803b63a1ee7060fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416300"
---
# <a name="imslogonopenentry"></a>IMSLogon::OpenEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Ordner oder ein Nachrichtenobjekt und gibt einen Zeiger auf das Objekt zurück, um weiteren Zugriff zu ermöglichen. 
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulOpenFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Größe des Eintragsbezeichners in Bytes, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Adresse des Eintragsbezeichners des zu öffnende Ordner- oder Nachrichtenobjekts. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID) für das Objekt. Das Übergeben von NULL gibt an, dass das Objekt in die Standardschnittstelle für ein solches Objekt übertragen wird. Der  _lpInterface-Parameter_ kann auch auf einen Bezeichner für eine geeignete Schnittstelle für das Objekt festgelegt werden. 
    
 _ulOpenFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Das Objekt sollte mit den maximal zulässigen Berechtigungen für den Benutzer und den maximalen Clientanwendungsberechtigungen geöffnet werden. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, wird das Objekt mit Lese-/Schreibberechtigung geöffnet. Wenn der Client über schreibgeschützte Berechtigungen verfügt, wird das Objekt mit schreibgeschützter Berechtigung geöffnet. Der Client kann die Berechtigungsstufe abrufen, indem er die **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) -Eigenschaft abruft.
    
MAPI_DEFERRED_ERRORS 
  
> Der Aufruf kann auch dann erfolgreich sein, wenn das zugrunde liegende Objekt für die aufrufende Anwendung nicht verfügbar ist. Wenn das Objekt nicht verfügbar ist, gibt ein nachfolgender Aufruf des Objekts möglicherweise einen Fehler zurück.
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigungen an. Standardmäßig werden Objekte mit schreibgeschützter Berechtigung erstellt, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigungen erteilt wurden. 
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> [out] Ein Zeiger auf den Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

MAPI ruft die **IMSLogon::OpenEntry-Methode** auf, um einen Ordner oder eine Nachricht in einem Nachrichtenspeicher zu öffnen. MAPI übergibt die Eintrags-ID des zu öffnende Objekts. Der Nachrichtenspeicheranbieter sollte einen Zeiger zurückgeben, der weiteren Zugriff auf das im  _lppUnk-Parameter_ angegebene Objekt ermöglicht. 
  
Bevor MAPI **IMSLogon::OpenEntry** aufruft, wird zunächst ermittelt, ob der angegebene Nachrichten- oder Ordnereintragsbezeichner mit einer von diesem Nachrichtenspeicheranbieter registrierten id entspricht. Weitere Informationen zum Registrieren von Eintragsbezeichnern durch Speicheranbieter finden Sie unter [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
  
 **IMSLogon::OpenEntry** ist identisch mit der [IMsgStore::OpenEntry-Methode](imsgstore-openentry.md) des Nachrichtenspeicherobjekts, mit der Ausnahme, dass der Client **IMSLogon::OpenEntry nicht aufruft.** MAPI ruft **IMSLogon::OpenEntry auf,** wenn eine **IMAPISession::OpenEntry-Methode verarbeitet** wird. Objekte, die mithilfe von **IMSLogon::OpenEntry** geöffnet werden, sollten genauso behandelt werden wie Objekte, die mithilfe des Nachrichtenspeicherobjekts geöffnet werden. Insbesondere Objekte, die mit diesem Aufruf geöffnet werden, sollten ungültig sein, wenn das Message Store-Objekt freigegeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

