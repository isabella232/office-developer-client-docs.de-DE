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
ms.openlocfilehash: 8b122c98715bd2f6916fe6302fc0b7a01d2cc936
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584611"
---
# <a name="imapisupportopenentry"></a>IMAPISupport::OpenEntry

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Öffnet ein Objekt und gibt einen Schnittstellenzeiger für den weiteren Zugriff. 
  
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
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Objekts zu öffnen.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, Zugriff auf das Objekt darstellt. Bei Übergabe von NULL führt das Objekt Standardschnittstelle zurückgegeben wird. Wenn das Objekt geöffnet werden soll, eine Nachricht ist, ist der standard-Benutzeroberfläche beispielsweise [IMessage](imessageimapiprop.md); Ordner ist es [IMAPIFolder](imapifolderimapicontainer.md). Die standard-Schnittstellen für Address Book-Objekten sind [IDistList](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser](imailuserimapiprop.md) für ein messaging-Benutzer. 
    
 _ulOpenFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt mit den maximale Netzwerkberechtigungen für den Anrufer zulässig geöffnet werden. Wenn der Aufrufer Lese-/Schreibberechtigung verfügt, sollte das Objekt beispielsweise mit Lese-/Schreibzugriff geöffnet werden; Wenn der Aufrufer nur-Lese-Berechtigung verfügt, sollte das Objekt als schreibgeschützt geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> **OpenEntry** erfolgreich, möglicherweise beendet, bevor das Objekt an den Anrufer vollständig zugegriffen werden kann. Wenn das Objekt nicht möglich ist, kann nachfolgende Objekt Anrufen ein Laufzeitfehler. 
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. In der Standardeinstellung Objekte werden als schreibgeschützt geöffnet, und Anrufer sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde. 
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des Objekts geöffnet.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern, oder es wurde versucht, ein Objekt zuzugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Es ist kein Objekt zugeordneten die Eintrags-ID in der _LpEntryID_ -Parameter übergeben. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die Eintrags-ID in der _LpEntryID_ -Parameter übergeben wird in einem Format nicht erkannt. Dieser Wert wird in der Regel zurückgegeben, wenn die Adressbuchanbieter, die das Objekt enthält nicht geöffnet ist. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::OpenEntry** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert. Dienstanbieter anrufen **IMAPISupport::OpenEntry** um einen Zeiger auf eine Schnittstelle abzurufen, die verwendet werden kann, um auf ein bestimmtes Objekt zuzugreifen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **IMAPISupport::OpenEntry** nur, wenn Sie nicht wissen, welche Art Objekt Sie öffnen möchten. Wenn Sie, dass Sie einen Ordner oder eine Nachricht öffnen wissen, rufen Sie stattdessen [IMsgStore::OpenEntry](imsgstore-openentry.md) . Wenn Sie, dass Sie ein Adressbuchcontainer, ein messaging-Benutzer oder eine Verteilerliste öffnen wissen, rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md). Diese bestimmten Methoden sind schneller als **IMAPISupport::OpenEntry**. 
  
 **IMAPISupport::OpenEntry** öffnet alle Objekte als schreibgeschützt, es sei denn, Sie legen Sie das Flag MAPI_MODIFY oder MAPI_BEST_ACCESS im _UlFlags_ -Parameter und Ihre Berechtigungen ausreichend sind. Festlegen einer dieser Flags garantiert keine bestimmte Art von Zugriff. die Berechtigungen, die Sie erteilt werden abhängig von Ihrer Zugriffsebene, die-Objekts und der Dienstanbieter, der das Objekt besitzt. Rufen Sie zum Bestimmen der Zugriffsebene des geöffneten-Objekts, dessen **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))-Eigenschaft ab.
  
Überprüfen Sie den Wert in der _LpulObjType_ -Parameter, um zu bestimmen, dass der Objekttyp zurückgegeben wird, was Sie erwartet zurückgegeben. Wenn der Objekttyp ist wie erwartet, wandeln Sie den Zeiger auf einen Zeiger des entsprechenden Typs aus dem _LppUnk_ -Parameter. Angenommen, wenn Sie einen Ordner öffnen, _LppUnk_ auf einen Zeiger vom Typ LPMAPIFOLDER umgewandelt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

