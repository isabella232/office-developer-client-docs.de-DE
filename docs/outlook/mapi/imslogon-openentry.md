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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317283"
---
# <a name="imslogonopenentry"></a>IMSLogon::OpenEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet ein Folder-oder Message-Objekt und gibt einen Zeiger auf das Objekt zurück, um weiteren Zugriff zu ermöglichen. 
  
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
  
> in Die Größe der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird, in Bytes. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Adresse der Eintrags-ID des zu öffnenden Folder-oder Message-Objekts. 
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID) für das Objekt. Übergeben von NULL gibt an, dass das Objekt für ein solches Objekt in die Standardschnittstelle umgewandelt wird. Der _lpInterface_ -Parameter kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für das Objekt festgelegt werden. 
    
 _ulOpenFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Das Objekt sollte mit den maximal zulässigen Berechtigungen für den Benutzer und den maximalen Client Anwendungsberechtigungen geöffnet werden. Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, wird das Objekt mit Lese-/Schreibzugriff geöffnet; Wenn der Client schreibgeschützte Berechtigung hat, wird das Objekt mit Leseberechtigung geöffnet. Der Client kann die Berechtigungsstufe abrufen, indem er die **PR_ACCESS_LEVEL** ([pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))-Eigenschaft abrufen.
    
MAPI_DEFERRED_ERRORS 
  
> Der Aufruf kann auch dann erfolgreich ausgeführt werden, wenn das zugrunde liegende Objekt für die aufrufende Anwendung nicht zur Verfügung steht. Wenn das Objekt nicht verfügbar ist, kann bei einem nachfolgenden Aufruf des Objekts ein Fehler zurückgegeben werden.
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Standardmäßig werden Objekte mit Leseberechtigung erstellt, und Clients sollten nicht unter der Annahme arbeiten, dass Lese-/Schreibzugriff erteilt wurde. 
    
 _lpulObjType_
  
> Out Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> Out Ein Zeiger auf den Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

MAPI Ruft die **IMSLogon:: OpenEntry** -Methode auf, um einen Ordner oder eine Nachricht in einem Nachrichtenspeicher zu öffnen. MAPI übergibt die Eintrags-ID des zu öffnenden Objekts. Der Nachrichtenspeicher Anbieter sollte einen Zeiger zurückgeben, der einen weiteren Zugriff auf das im _lppUnk_ -Parameter angegebene Objekt ermöglicht. 
  
Bevor MAPI **IMSLogon:: OpenEntry**aufruft, bestimmt es zunächst, ob der angegebene Nachricht-oder Ordnereintrags Bezeichner einem von diesem Nachrichtenspeicher Anbieter registrierten entspricht. Weitere Informationen dazu, wie Speicheranbieter Eintrags-IDs registrieren, finden Sie unter [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md).
  
 **IMSLogon:: OpenEntry** ist identisch mit der [IMsgStore:: OpenEntry](imsgstore-openentry.md) -Methode des Nachrichtenspeicher Objekts, es sei denn, der Client ruft **IMSLogon:: OpenEntry**; MAPI ruft **IMSLogon:: OpenEntry** auf, wenn es eine **IMAPISession:: OpenEntry** -Methode verarbeitet. Objekte, die mit **IMSLogon:: OpenEntry** geöffnet werden, sollten genau wie Objekte behandelt werden, die mit dem Nachrichtenspeicherobjekt geöffnet wurden; insbesondere werden Objekte, die mit diesem Aufruf geöffnet werden, beim Freigeben des Nachrichtenspeicher Objekts für ungültig erklärt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

