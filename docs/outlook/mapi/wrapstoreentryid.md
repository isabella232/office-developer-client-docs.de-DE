---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325669"
---
# <a name="wrapstoreentryid"></a>WrapStoreEntryID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konvertiert die interne Eintrags-ID eines Nachrichtenspeichers in eine Eintrags-ID, die vom Messagingsystem nutzbar ist. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
WrapStoreEntryID(
  ULONG ulFlags,
  LPSTR szDLLName,
  ULONG cbOrigEntry,
  LPENTRYID lpOrigEntry,
  ULONG * lpcbWrappedEntry,
  LPENTRYID * lppWrappedEntry
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Bitmaske von Flags. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format. 
    
 _szDLLName_
  
> in Der Name der DLL des Nachrichtenspeicher Anbieters. 
    
 _cbOrigEntry_
  
> in Größe (in Bytes) der ursprünglichen Eintrags-ID für den Nachrichtenspeicher. 
    
 _lpOrigEntry_
  
> in Zeiger auf eine [Eintrags](entryid.md) -ID-Struktur, die den ursprünglichen Eintragsbezeichner enthält. 
    
 _lpcbWrappedEntry_
  
> Out Zeiger auf die Größe des neuen Eintrags Bezeichners in Bytes. 
    
 _lppWrappedEntry_
  
> Out Zeiger auf einen Zeiger auf eine **Eintrags** -ID-Struktur, die den neuen Eintragsbezeichner enthält. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Ein Nachrichtenspeicherobjekt behält eine interne Eintrags-ID bei, die nur für Dienstanbieter von Bedeutung ist, die mit diesem Nachrichtenspeicher in Kontakt stehen. Für andere Messagingkomponenten stellt MAPI eine verpackte Version des internen Eintrags Bezeichners zur Verdeutlichung bereit, die dem Nachrichtenspeicher zugeordnet ist. Der Anbieter für die Bereitstellen von Dienstanbietern sollte immer den ursprünglichen, unverpackten Nachrichtenspeicher Eintragsbezeichner erhalten. Clientanwendungen sollten immer die verpackte Version erhalten, die dann an beliebiger Stelle in der Messaging Domäne und in anderen Domänen verwendet werden kann. 
  
Ein Dienstanbieter kann einen Eintragsbezeichner für den Nachrichtenspeicher mit der **WrapStoreEntryID** -Funktion oder der [IMAPISupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md) -Methode, die die **WrapStoreEntryID** -Funktion aufruft, umschließen. Der Anbieter muss die Eintrags-ID umbrechen, wenn die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft des Nachrichtenspeichers verfügbar gemacht oder in einen Profil Abschnitt geschrieben wird und das **PR_STORE_ENTRYID** ([pidtagstoreentryid (](pidtagstoreentryid-canonical-property.md)) Eigenschaft. MAPI umschließt eine Nachrichtenspeicher-Eintrags-ID, wenn auf einen [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) -Aufruf reagiert wird. 
  
Wenn eine Clientanwendung einen eingebundenen Nachrichtenspeicher-Eintragsbezeichner an MAPI übergibt, beispielsweise in einem [IMAPISession:: OpenEntry](imapisession-openentry.md) -Aufruf, wird die Eintrags-ID von MAPI vor der Verwendung zum Aufrufen einer Anbietermethode wie [IMSProvider:: LOGON](imsprovider-logon.md) oder [ IMSProvider:: CompareStoreIDs](imsprovider-comparestoreids.md). 
  

