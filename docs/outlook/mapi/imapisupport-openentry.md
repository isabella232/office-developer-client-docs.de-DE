---
title: IMAPISupportOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cfbb799336aa1e75fa36e03e55d82c3af3409f10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326346"
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des zu öffnenden Objekts.
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll. Übergeben von NULL Ergebnisse in der Standardschnittstelle des Objekts zurückgegeben wird. Wenn das zu öffnende Objekt beispielsweise eine Nachricht ist, ist die Standardschnittstelle [IMessage](imessageimapiprop.md); für Ordner ist es [IMAPIFolder](imapifolderimapicontainer.md). Die Standardschnittstellen für Adressbuch Objekte sind [IDistList](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser](imailuserimapiprop.md) für einen Messagingbenutzer. 
    
 _ulOpenFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Fordert, dass das Objekt mit den maximal zulässigen Netzwerkberechtigungen für den Anrufer geöffnet wird. Wenn der Aufrufer beispielsweise über Lese-/Schreibzugriff verfügt, sollte das Objekt als Lese-/Schreibzugriff geöffnet werden; Wenn der Aufrufer schreibgeschützte Berechtigung hat, sollte das Objekt schreibgeschützt geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **** das erfolgreiche zurückgeben von OpenEntry, möglicherweise vor dem vollständigen Zugriff auf das Objekt für den Aufrufer. Wenn auf das Objekt nicht zugegriffen werden kann, führt ein nachfolgendes Objektaufruf zu einem Fehler. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Standardmäßig werden Objekte als schreibgeschützt geöffnet, und Anrufer sollten nicht unter der Annahme arbeiten, dass die Berechtigung "Lese-/Schreibzugriff" erteilt wurde. 
    
 _lpulObjType_
  
> Out Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> Out Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern, oder es wurde versucht, auf ein Objekt zuzugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Es ist kein Objekt mit der im _lpEntryID_ -Parameter übergebenen Eintrags-ID verknüpft. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die im _lpEntryID_ -Parameter übergebene Eintrags-ID weist ein unbekanntes Format auf. Dieser Wert wird in der Regel zurückgegeben, wenn der Adressbuchanbieter, der das Objekt enthält, nicht geöffnet ist. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: OpenEntry** -Methode wird für alle Support Objekte des Dienstanbieters implementiert. Dienstanbieter rufen **IMAPISupport:: OpenEntry** auf, um einen Zeiger auf eine Schnittstelle abzurufen, die für den Zugriff auf ein bestimmtes Objekt verwendet werden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **IMAPISupport:: OpenEntry** nur auf, wenn Sie nicht wissen, welche Art von Objekt Sie öffnen. Wenn Sie wissen, dass Sie einen Ordner oder eine Nachricht öffnen möchten, rufen Sie stattdessen [IMsgStore:: OpenEntry](imsgstore-openentry.md) auf. Wenn Sie wissen, dass Sie einen Adressbuchcontainer, einen Messagingbenutzer oder eine Verteilerliste öffnen, rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md)auf. Diese spezifischeren Methoden sind schneller als **IMAPISupport:: OpenEntry**. 
  
 **IMAPISupport:: OpenEntry** öffnet alle Objekte schreibgeschützt, es sei denn, Sie legen das MAPI_MODIFY-oder MAPI_BEST_ACCESS-Flag im Parameter _ulFlags_ fest und ihre Berechtigungen sind ausreichend. Das Festlegen eines dieser Flags garantiert keinen bestimmten Zugriffstyp. die Berechtigungen, die Ihnen erteilt werden, hängen von ihrer Zugriffsebene, dem Objekt und dem Dienstanbieter ab, der das Objekt besitzt. Um die Zugriffsebene des geöffneten Objekts zu bestimmen, rufen Sie die **PR_ACCESS_LEVEL** ([pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))-Eigenschaft ab.
  
Überprüfen Sie den Wert, der im _lpulObjType_ -Parameter zurückgegeben wird, um zu ermitteln, ob der zurückgegebene Objekttyp Ihren Erwartungen entspricht. Wenn der Objekttyp erwartungsgemäß ist, wandeln Sie den Zeiger vom _lppUnk_ -Parameter in einen Zeiger des entsprechenden Typs um. Wenn Sie beispielsweise einen Ordner öffnen, werfen Sie _lppUnk_ in einen Zeiger vom Typ LPMAPIFOLDER. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

