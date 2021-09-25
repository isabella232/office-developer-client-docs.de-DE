---
title: IMAPISupportOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f32669886f3272420c10e410d64a6ce8a7fac0a5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592403"
---
# <a name="imapisupportopenentry"></a>IMAPISupport::OpenEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet ein Objekt und gibt einen Schnittstellenzeiger für den weiteren Zugriff zurück. 
  
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
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des zu öffnenden Objekts.
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll. Wenn NULL übergeben wird, wird die Standardschnittstelle des Objekts zurückgegeben. Wenn das zu öffnende Objekt z. B. eine Nachricht ist, ist die Standardschnittstelle [IMessage](imessageimapiprop.md); für Ordner ist dies [IMAPIFolder](imapifolderimapicontainer.md). Die Standardschnittstellen für Adressbuchobjekte sind [IDistList](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser](imailuserimapiprop.md) für einen Messagingbenutzer. 
    
 _ulOpenFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt mit den für den Aufrufer maximal zulässigen Netzwerkberechtigungen geöffnet wird. Wenn der Aufrufer beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte das Objekt mit Lese-/Schreibzugriff geöffnet werden. Wenn der Aufrufer über schreibgeschützte Berechtigungen verfügt, sollte das Objekt schreibgeschützt geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenEntry** die erfolgreiche Rückgabe, möglicherweise bevor für den Aufrufer vollständig auf das Objekt zugegriffen werden kann. Wenn auf das Objekt nicht zugegriffen werden kann, kann das Ausführen eines nachfolgenden Objektaufrufs zu einem Fehler führen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Standardmäßig werden Objekte schreibgeschützt geöffnet, und Aufrufer sollten nicht mit der Annahme arbeiten, dass Lese-/Schreibberechtigung erteilt wurde. 
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern, oder es wurde versucht, auf ein Objekt zuzugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Es ist kein Objekt mit dem Eintragsbezeichner verknüpft, der im  _lpEntryID-Parameter_ übergeben wird. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der im  _lpEntryID-Parameter_ übergebene Eintragsbezeichner weist ein nicht erkennbares Format auf. Dieser Wert wird in der Regel zurückgegeben, wenn der Adressbuchanbieter, der das Objekt enthält, nicht geöffnet ist. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::OpenEntry-Methode** ist für alle Dienstanbieter-Supportobjekte implementiert. Dienstanbieter rufen **IMAPISupport::OpenEntry** auf, um einen Zeiger auf eine Schnittstelle abzurufen, die für den Zugriff auf ein bestimmtes Objekt verwendet werden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **IMAPISupport::OpenEntry** nur auf, wenn Sie nicht wissen, welche Art von Objekt Sie öffnen. Wenn Sie wissen, dass Sie einen Ordner oder eine Nachricht öffnen, rufen Sie stattdessen [IMsgStore::OpenEntry](imsgstore-openentry.md) auf. Wenn Sie wissen, dass Sie einen Adressbuchcontainer, einen Messagingbenutzer oder eine Verteilerliste öffnen, rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md)auf. Diese spezifischeren Methoden sind schneller als **IMAPISupport::OpenEntry**. 
  
 **IMAPISupport::OpenEntry** öffnet alle Objekte schreibgeschützt, es sei denn, Sie legen das flag MAPI_MODIFY oder MAPI_BEST_ACCESS im  _UlFlags-Parameter_ fest, und Ihre Berechtigungen sind ausreichend. Das Festlegen eines dieser Flags garantiert keinen bestimmten Zugriffstyp. Welche Berechtigungen Ihnen erteilt werden, hängt von Der Zugriffsebene, dem Objekt und dem Dienstanbieter ab, der das Objekt besitzt. Um die Zugriffsebene des geöffneten Objekts zu bestimmen, rufen Sie dessen **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) -Eigenschaft ab.
  
Überprüfen Sie den im  _Parameter "lpulObjType"_ zurückgegebenen Wert, um zu ermitteln, ob der zurückgegebene Objekttyp dem erwarteten Entspricht. Wenn der Objekttyp wie erwartet ist, wandeln Sie den Zeiger vom  _lppUnk-Parameter_ in einen Zeiger des entsprechenden Typs um. Wenn Sie beispielsweise einen Ordner öffnen, wandeln Sie  _lppUnk_ in einen Zeiger vom Typ LPMAPIFOLDER um. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

