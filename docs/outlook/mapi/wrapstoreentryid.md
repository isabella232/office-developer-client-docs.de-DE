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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 45263396e69852a9ae17ff6fce284663bdf2fb07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585136"
---
# <a name="wrapstoreentryid"></a>WrapStoreEntryID

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Konvertiert einen Nachrichtenspeicher interne Eintrags-ID auf einen Eintrag Bezeichner Verwendbarkeit von messaging-System. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
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
  
> [in] Bitmaske der Kennzeichen. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format. 
    
 _szDLLName_
  
> [in] Der Name des Anbieters Nachricht DLL. 
    
 _cbOrigEntry_
  
> [in] Größe des den ursprünglichen Eintrag Bezeichner für den Nachrichtenspeicher in Bytes. 
    
 _lpOrigEntry_
  
> [in] Zeiger auf eine [ENTRYID](entryid.md) -Struktur, die die ursprünglichen Eintrags-ID enthält. 
    
 _lpcbWrappedEntry_
  
> [out] Zeiger auf die Größe des neuen Eintrags-ID in Bytes. 
    
 _lppWrappedEntry_
  
> [out] Zeiger auf einen Zeiger auf eine **ENTRYID** -Struktur, die die neue Eintrags-ID enthält. 
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>HinwBemerkungeneise

Ein Meldungsobjekt Store behält eine interne Eintrags-ID der nur für Service Provider Coresident mit diesem Nachrichtenspeicher von Bedeutung ist. Für andere Messagingkomponenten stellt MAPI eine gepackten Version von der internen Eintrags-ID, mit die Hilfe erkennbar wie, mit dem Nachrichtenspeicher gehören. Coresident-Dienstanbieter müssen immer die ursprünglichen allein stehenden Store Eintrags-ID angegeben werden; Clientanwendungen sollte immer die gepackten Version angegeben werden, die dann verwendbar an einer beliebigen Stelle in der messaging-Domäne und in anderen Domänen. 
  
Ein Dienstanbieter kann umschließen eine Nachricht Store Eintrag ID mit der Funktion **WrapStoreEntryID** oder die [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) -Methode, die die **WrapStoreEntryID** -Funktion aufruft. Der Anbieter muss die Eintrags-ID umbrochen, wenn der Nachrichtenspeicher **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) Verfügbarmachen-Eigenschaft oder Schreiben in einem Profilabschnitt und, **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) verfügbar zu machen. -Eigenschaft. MAPI umbrochen eine Nachricht Store Eintrags-ID wird, wenn Sie einem Anruf [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) reagiert. 
  
Wenn eine Clientanwendung eine gepackten Store Eintrags-ID MAPI übergibt, entpackt beispielsweise einen Aufruf [IMAPISession::OpenEntry](imapisession-openentry.md) MAPI die Eintrags-ID vor der Verwendung eine Anbieter-Methode wie [IMSProvider::Logon](imsprovider-logon.md) oder [aufrufen IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md). 
  

