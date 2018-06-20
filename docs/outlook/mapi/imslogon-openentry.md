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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e9d9ca56a877c0106c76242fe97ce43321e62e08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792673"
---
# <a name="imslogonopenentry"></a>IMSLogon::OpenEntry

  
  
**Betrifft**: Outlook 
  
Öffnet einen Ordner oder Message-Objekt und gibt einen Zeiger auf das Objekt, das Zugriff zu ermöglichen. 
  
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
  
> [in] Die Größe des Eintrags-ID, die auf das durch den Parameter _LpEntryID_ in Bytes. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Adresse des Eintrags-ID des Objekts Ordner oder eine Nachricht zu öffnen. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf der Benutzeroberfläche IID (Identifier) für das Objekt. Übergeben von NULL gibt an, dass das Objekt in der standard-Benutzeroberfläche für ein solches Objekt umgewandelt wird. Der Parameter _LpInterface_ kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für das Objekt festgelegt werden. 
    
 _ulOpenFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Das Objekt sollte mit den maximalen Berechtigungen für den Benutzer und die maximale Clientberechtigungen zulässigen geöffnet werden. Wenn der Client über Lese-/Schreibberechtigung verfügt, wird das Objekt beispielsweise mit Lese-/Schreibzugriff geöffnet. Wenn der Client nur-Lese-Berechtigung verfügt, wird das Objekt mit Leseberechtigung geöffnet. Der Client kann die Berechtigungsstufe Abrufen der **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))-Eigenschaft abrufen.
    
MAPI_DEFERRED_ERRORS 
  
> Der Aufruf ist zulässig, erfolgreich ausgeführt werden kann, auch wenn das zugrunde liegende Objekt nicht an die aufrufende Anwendung verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann ein nachfolgender Aufruf für das Objekt einen Fehler zurück.
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. Standardmäßig werden Objekte mit Leseberechtigung erstellt, und Clients sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde. 
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des Objekts geöffnet.
    
 _lppUnk_
  
> [out] Ein Zeiger auf den Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

MAPI-Aufrufen die **IMSLogon::OpenEntry** -Methode, um einen Ordner oder eine Nachricht in einem Nachrichtenspeicher zu öffnen. MAPI übergibt die Eintrags-ID des Objekts zu öffnen. Der Nachricht Speicheranbieter sollte einen Zeiger zurückgegeben, der die weiteren Zugriff auf das Objekt im _LppUnk_ -Parameter angegebene ermöglicht. 
  
Bevor MAPI **IMSLogon::OpenEntry**aufruft, bestimmt zunächst, dass die angegebenen Nachricht oder Ordner Eintrags-ID eine durch diese Nachricht Speicheranbieter registrierten übereinstimmt. Weitere Informationen dazu, wie Anbieter Eintragsbezeichner registrieren finden Sie unter [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
  
 **IMSLogon::OpenEntry** ist identisch mit der [IMsgStore::OpenEntry](imsgstore-openentry.md) -Methode des Message Store-Objekts, mit der Ausnahme, dass der Client nicht **IMSLogon::OpenEntry**aufgerufen wird. MAPI-Aufrufen **IMSLogon::OpenEntry** bei der Verarbeitung einer **IMAPISession::OpenEntry** -Methode. Objekte, die mithilfe von **IMSLogon::OpenEntry** geöffnet werden sollte behandelt genau wie Speichern von Objekten, die mit der Meldung geöffnet-Objekt. Insbesondere sollten Objekte, die mithilfe dieses Anrufs geöffnet ungültig gemacht werden, wenn das Store-Nachrichtenspeicherobjekt freigegeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon: IUnknown](imslogoniunknown.md)

