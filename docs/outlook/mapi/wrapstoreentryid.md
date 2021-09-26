---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ef6286738be70ee3e2d91d32df9635f25df0a6c7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583233"
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
  
> [in] Bitmaske von Flags. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format. 
    
 _szDLLName_
  
> [in] Der Name der DLL des Nachrichtenspeicheranbieters. 
    
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
  
## <a name="remarks"></a>HinwBemerkungeneise

Ein Nachrichtenspeicherobjekt behält einen internen Eintragsbezeichner bei, der nur für den Kern des Dienstanbieters mit diesem Nachrichtenspeicher von Bedeutung ist. Für andere Messagingkomponenten stellt MAPI eine umschlossene Version des internen Eintragsbezeichners bereit, die erkennbar macht, dass sie zum Nachrichtenspeicher gehört. Kernsident-Dienstanbieter sollten immer den ursprünglichen ungepackten Eintragsbezeichner für den Nachrichtenspeicher erhalten. Clientanwendungen sollte immer die umschlossene Version zur Verfügung gestellt werden, die dann überall in der Messagingdomäne und in anderen Domänen verwendet werden kann. 
  
Ein Dienstanbieter kann einen Eintragsbezeichner für den Nachrichtenspeicher mithilfe der **WrapStoreEntryID-Funktion** oder der [IMAPISupport::WrapStoreEntryID-Methode umschließen,](imapisupport-wrapstoreentryid.md) die die **WrapStoreEntryID-Funktion aufruft.** Der Anbieter muss den Eintragsbezeichner umschließen, wenn er die **Eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) des Nachrichtenspeichers verfügbar macht oder in einen Profilabschnitt schreibt und wenn die **eigenschaft PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) verfügbar wird. MAPI umschließt einen Eintragsbezeichner für den Nachrichtenspeicher, wenn auf einen [IMAPISession::OpenMsgStore-Aufruf](imapisession-openmsgstore.md) reagiert wird. 
  
Wenn eine Clientanwendung einen umschlossenen Eintragsbezeichner für den Nachrichtenspeicher an die MAPI übergibt, z. B. in einem [IMAPISession::OpenEntry-Aufruf,](imapisession-openentry.md) hebt MAPI den Eintragsbezeichner auf, bevor sie zum Aufrufen einer Anbietermethode wie [IMSProvider::Logon](imsprovider-logon.md) oder [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md)verwendet wird. 
  

