---
title: IMSLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon.OpenEntry
api_type:
- COM
ms.assetid: 612cbab7-60cb-48bb-906e-18d9135e7a86
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 560d68693589b5fc4daef8c6f440147b6fe9283a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551184"
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
  
> [in] Die Größe (in Byte) des Eintragsbezeichners, auf den der  _parameter lpEntryID_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Adresse des Eintragsbezeichners des zu öffnenden Ordner- oder Nachrichtenobjekts. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID) für das Objekt. Wenn NULL übergeben wird, wird angegeben, dass das Objekt in die Standardschnittstelle für ein solches Objekt umgewandelt wird. Der  _lpInterface-Parameter_ kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für das Objekt festgelegt werden. 
    
 _ulOpenFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Das Objekt sollte mit den maximal zulässigen Berechtigungen für den Benutzer und den maximalen Clientanwendungsberechtigungen geöffnet werden. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, wird das Objekt mit Lese-/Schreibberechtigung geöffnet. wenn der Client über schreibgeschützte Berechtigungen verfügt, wird das Objekt mit schreibgeschützter Berechtigung geöffnet. Der Client kann die Berechtigungsstufe abrufen, indem er die **eigenschaft PR_ACCESS_LEVEL** ([PidTagAccessLevel ) abruft.](pidtagaccesslevel-canonical-property.md)
    
MAPI_DEFERRED_ERRORS 
  
> Der Aufruf kann auch dann erfolgreich ausgeführt werden, wenn das zugrunde liegende Objekt für die aufrufende Anwendung nicht verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann ein nachfolgender Aufruf des Objekts einen Fehler zurückgeben.
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Standardmäßig werden Objekte mit schreibgeschützter Berechtigung erstellt, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigung erteilt wurde. 
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> [out] Ein Zeiger auf den Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

MAPI ruft die **IMSLogon::OpenEntry-Methode** auf, um einen Ordner oder eine Nachricht in einem Nachrichtenspeicher zu öffnen. MAPI übergibt den Eintragsbezeichner des zu öffnenden Objekts. Der Nachrichtenspeicheranbieter sollte einen Zeiger zurückgeben, der weiteren Zugriff auf das im  _lppUnk-Parameter_ angegebene Objekt ermöglicht. 
  
Bevor DIE MAPI **IMSLogon::OpenEntry** aufruft, wird zuerst ermittelt, dass der angegebene Nachrichten- oder Ordnereintragsbezeichner mit dem bezeichner übereinstimmt, der von diesem Nachrichtenspeicheranbieter registriert wurde. Weitere Informationen dazu, wie Speicheranbieter Eintragsbezeichner registrieren, finden Sie unter [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
  
 **IMSLogon::OpenEntry** ist identisch mit der [IMsgStore::OpenEntry-Methode](imsgstore-openentry.md) des Nachrichtenspeicherobjekts, mit der Ausnahme, dass der Client **IMSLogon::OpenEntry nicht aufruft;** MAPI ruft **IMSLogon::OpenEntry** auf, wenn eine **IMAPISession::OpenEntry-Methode** verarbeitet wird. Objekte, die mithilfe von **IMSLogon::OpenEntry** geöffnet werden, sollten genauso behandelt werden wie Objekte, die mithilfe des Nachrichtenspeicherobjekts geöffnet wurden. Insbesondere sollten Objekte, die mithilfe dieses Aufrufs geöffnet werden, ungültig werden, wenn das Nachrichtenspeicherobjekt freigegeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

