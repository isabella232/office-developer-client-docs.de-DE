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
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409209"
---
# <a name="wrapstoreentryid"></a>WrapStoreEntryID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konvertiert den internen Eintragsbezeichner eines Nachrichtenspeichers in einen Eintragsbezeichner, der vom Messagingsystem besser verwendet werden kann. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
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
  
> [in] Bitmaske von Flags. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format. 
    
 _szDLLName_
  
> [in] Der Name der Nachrichtenspeicheranbieter-DLL. 
    
 _cbOrigEntry_
  
> [in] Größe des ursprünglichen Eintragsbezeichners für den Nachrichtenspeicher in Bytes. 
    
 _lpOrigEntry_
  
> [in] Zeiger auf eine [ENTRYID-Struktur,](entryid.md) die den ursprünglichen Eintragsbezeichner enthält. 
    
 _lpcbWrappedEntry_
  
> [out] Zeiger auf die Größe des neuen Eintragsbezeichners in Bytes. 
    
 _lppWrappedEntry_
  
> [out] Zeiger auf einen Zeiger auf eine **ENTRYID-Struktur,** die den neuen Eintragsbezeichner enthält. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

Ein Nachrichtenspeicherobjekt behält einen internen Eintragsbezeichner bei, der nur für Dienstanbieter sinnvoll ist, die mit diesem Nachrichtenspeicher zusammenarbeiten. Für andere Messagingkomponenten stellt MAPI eine umschlossene Version des internen Eintragsbezeichners zur Verfügung, die ihn als zum Nachrichtenspeicher gehörig erkennbar macht. Coresident-Dienstanbieter sollten immer den ursprünglichen eintragsbezeichner des nachrichtenspeichers erhalten. Clientanwendungen sollten immer die umschlossene Version erhalten, die dann überall in der Messagingdomäne und in anderen Domänen verwendet werden kann. 
  
Ein Dienstanbieter kann einen Nachrichtenspeichereintragsbezeichner mithilfe der **WrapStoreEntryID-Funktion** oder der [IMAPISupport::WrapStoreEntryID-Methode](imapisupport-wrapstoreentryid.md) umschließen, die die **WrapStoreEntryID-Funktion** aufruft. Der Anbieter muss die Eintrags-ID umschließen, wenn die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft des Nachrichtenspeichers verfügbar ist oder in einen Profilabschnitt geschrieben wird, und wenn die **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) -Eigenschaft verfügbar ist. MAPI umschließt einen Nachrichtenspeichereintragsbezeichner, wenn auf einen [IMAPISession::OpenMsgStore-Aufruf reagiert](imapisession-openmsgstore.md) wird. 
  
Wenn eine Clientanwendung einen umschlossenen Nachrichtenspeichereintragsbezeichner an MAPI übergibt, z. B. in einem [IMAPISession::OpenEntry-Aufruf,](imapisession-openentry.md) entpackt MAPI den Eintragsbezeichner, bevor er zum Aufrufen einer Anbietermethode wie [IMSProvider::Logon](imsprovider-logon.md) oder [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md)verwendet wird. 
  

