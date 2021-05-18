---
title: IMAPISupportAddress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Address
api_type:
- COM
ms.assetid: 8c22547e-ddf5-47f7-aed3-76e3854688df
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7300c11d5835640fe308430c9bb08d40b397e47b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407319"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt das Dialogfeld allgemeine Adresse an. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parameter

 _lpulUIParam_
  
> [in, out] Ein Zeiger auf das Handle des übergeordneten Fensters des Dialogfelds. Bei der Eingabe muss immer ein Fensterhandle übergeben werden. Wenn bei der Ausgabe das DIALOG_SDI in der [ADRPARM-Struktur](adrparm.md) festgelegt ist, auf die der  _lpAdrParms-Parameter_ verweist, wird das Fensterhandle des Dialogfelds ohne Modus zurückgegeben. 
    
 _lpAdrParms_
  
> [in, out] Ein Zeiger auf eine **ADRPARM-Struktur,** die die Präsentation und das Verhalten des Adressdialogfelds steuert. 
    
 _lppAdrList_
  
> [in, out] Ein Zeiger auf einen Zeiger auf eine Adressliste. Bei der Eingabe ist diese Liste entweder die aktuelle Liste der Empfänger in einer Nachricht oder NULL, wenn keine solche Liste vorhanden ist. Bei der Ausgabe  _zeigt lppAdrList_ auf eine aktualisierte Liste von Nachrichtenempfängern. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Dialogfeld Adresse wurde erfolgreich angezeigt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::Address-Methode** wird für Unterstützungsobjekte des Adressbuchanbieters implementiert. Adressbuchanbieter rufen **Address auf,** um eine Liste von Nachrichtenempfängern zu erstellen oder zu aktualisieren. 
  
Jeder Empfänger wird in einer [ADRENTRY-Struktur](adrentry.md) beschrieben, die in der [ADRLIST-Struktur](adrlist.md) enthalten ist, auf die der  _lppAdrList-Parameter_ verweist. Die **ADRENTRY-Struktur** enthält ein Array von Empfängereigenschaftswerten, von denen einer der Typ des Empfängers oder PR_RECIPIENT_TYPE **(** [PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) -Eigenschaft ist. Diese **ADRLIST-Struktur** kann an einen Client übergeben werden, der als _lpMods-Parameter_ in einem Aufruf von [IMessage::ModifyRecipients verwendet wird.](imessage-modifyrecipients.md)
  
Jeder Empfänger in der **ADRLIST-Struktur** kann entweder aufgelöst werden, was angibt, dass einer der Eigenschaftswerte seine **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft ist, oder nicht aufgelöst, was angibt, dass die **PR_ENTRYID-Eigenschaft** fehlt. 
  
Zusätzlich zu **PR_ENTRYID** enthalten aufgelöste Empfänger die folgenden Eigenschaften:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Nicht aufgelöste Empfänger enthalten in der Regel **nur PR_DISPLAY_NAME** und **PR_RECIPIENT_TYPE**. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **ADRLIST-Struktur,** die der Aufrufer übergibt, kann eine andere Größe als die von MAPI zurückgegebene Struktur aufweisen. Wenn Sie speicher für die **ADRLIST-Struktur zuweisen,** weisen Sie den Arbeitsspeicher für jede [SPropValue-Struktur](spropvalue.md) separat zu. 
  
Verwenden Sie die Zeiger auf die AN IHRE [ABProviderInit-Funktion übergebenen](abproviderinit.md) MAPI-Speicherzuweisungsfunktionen, um Arbeitsspeicher zuzuordnen. Zuordnen von Arbeitsspeicher mit der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) für **ADRLIST** und jeder Eigenschaftswertstruktur in den **ADRENTRY-Strukturen** in **ADRLIST**. 
  
Wenn **Address** eine größere **ADRLIST-Struktur** zurückgeben muss oder Wenn Sie NULL für  _lppAdrList_ übergeben haben, gibt **Address** die ursprüngliche Struktur frei und weist eine neue zu. **Address** weist außerdem zusätzliche Eigenschaftenwertstrukturen in der **ADRLIST-Struktur** zu und gibt alte Werte frei. Weitere Informationen zur Verwaltung des Arbeitsspeichers für **ADRLIST-Strukturen** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
 **Address** gibt sofort zurück, wenn DIALOG_SDI in der **ADRPARM-Struktur** im  _lpAdrParms-Parameter festgelegt_ wurde. 
  
## <a name="see-also"></a>Siehe auch



[ABProviderInit](abproviderinit.md)
  
[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[ADRPARM](adrparm.md)
  
[FreePadrlist](freepadrlist.md)
  
[FreeProws](freeprows.md)
  
[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagAddressType (kanonische Eigenschaft)](pidtagaddresstype-canonical-property.md)
  
[PidTagDisplayName (kanonische Eigenschaft)](pidtagdisplayname-canonical-property.md)
  
[PidTagDisplayType (kanonische Eigenschaft)](pidtagdisplaytype-canonical-property.md)
  
[PidTagEntryId (kanonische Eigenschaft)](pidtagentryid-canonical-property.md)
  
[PidTagRecipientType (kanonische Eigenschaft)](pidtagrecipienttype-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Verwalten des Arbeitsspeichers für ADRLIST- und SRowSet-Strukturen](managing-memory-for-adrlist-and-srowset-structures.md)

