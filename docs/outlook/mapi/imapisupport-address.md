---
title: IMAPISupportAddress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.Address
api_type:
- COM
ms.assetid: 8c22547e-ddf5-47f7-aed3-76e3854688df
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ee1a45deedc733d016d20fbd5cb43dbfa3b6b495
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625490"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt das allgemeine Adressdialogfeld an. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parameter

 _lpulUIParam_
  
> [in, out] Ein Zeiger auf das Handle des übergeordneten Fensters des Dialogfelds. Bei der Eingabe muss immer ein Fensterhandle übergeben werden. Wenn bei der Ausgabe das DIALOG_SDI-Kennzeichen in der [ADRPARM-Struktur](adrparm.md) festgelegt ist, auf die der  _lpAdrParms-Parameter_ verweist, wird das Fensterhandle des Dialogfelds ohne Modus zurückgegeben. 
    
 _lpAdrParms_
  
> [in, out] Ein Zeiger auf eine **ADRPARM-Struktur,** die die Darstellung und das Verhalten des Adressdialogfelds steuert. 
    
 _lppAdrList_
  
> [in, out] Ein Zeiger auf einen Zeiger auf eine Adressliste. Bei der Eingabe ist diese Liste entweder die aktuelle Liste der Empfänger in einer Nachricht oder NULL, wenn keine solche Liste vorhanden ist. Bei der Ausgabe verweist  _lppAdrList_ auf eine aktualisierte Liste der Nachrichtenempfänger. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Adressdialogfeld wurde erfolgreich angezeigt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::Address-Methode** ist für Supportobjekte des Adressbuchanbieters implementiert. Adressbuchanbieter rufen **"Adresse"** auf, um eine Liste von Nachrichtenempfängern zu erstellen oder zu aktualisieren. 
  
Jeder Empfänger wird in einer [ADRENTRY-Struktur](adrentry.md) beschrieben, die in der [ADRLIST-Struktur](adrlist.md) enthalten ist, auf die durch den  _lppAdrList-Parameter_ verwiesen wird. Die **ADRENTRY-Struktur** enthält ein Array von Empfängereigenschaftswerten, von denen einer der Typ des Empfängers oder **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) -Eigenschaft ist. Diese **ADRLIST-Struktur** kann an einen Client übergeben werden, um sie als  _lpMods-Parameter_ in einem Aufruf von [IMessage::ModifyRecipients](imessage-modifyrecipients.md)zu verwenden.
  
Jeder Empfänger in der **ADRLIST-Struktur** kann entweder aufgelöst werden, was bedeutet, dass einer seiner Eigenschaftswerte die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft ist, oder nicht aufgelöst, was darauf hinweist, dass die **PR_ENTRYID-Eigenschaft** fehlt. 
  
Zusätzlich zu **PR_ENTRYID** enthalten aufgelöste Empfänger die folgenden Eigenschaften:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Nicht aufgelöste Empfänger enthalten in der Regel nur **PR_DISPLAY_NAME** und **PR_RECIPIENT_TYPE.** 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **ADRLIST-Struktur,** die der Aufrufer übergibt, kann eine andere Größe als die von der MAPI zurückgegebene Struktur aufweisen. Wenn Sie Speicher für die **ADRLIST-Struktur** zuordnen, weisen Sie den Speicher für jede [SPropValue-Struktur](spropvalue.md) separat zu. 
  
Verwenden Sie die Zeiger auf die MAPI-Speicherzuweisungsfunktionen, die an Ihre [ABProviderInit-Funktion](abproviderinit.md) übergeben werden, um Speicher zuzuweisen. Weisen Sie Speicher mit der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) für **ADRLIST** und jede Eigenschaftswertstruktur in den **ADRENTRY-Strukturen** in **ADRLIST zu.** 
  
Wenn **Address** eine größere **ADRLIST-Struktur** zurückgeben muss oder wenn Sie NULL für  _lppAdrList_ übergeben haben, gibt **Address** die ursprüngliche Struktur frei und weist eine neue struktur zu. **Die Adresse** weist außerdem zusätzliche Eigenschaftswertstrukturen in der **ADRLIST-Struktur** zu und gibt die alten nach Bedarf frei. Weitere Informationen dazu, wie Speicher für **ADRLIST-Strukturen** verwaltet wird, finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
 **Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter. 
  
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
  
[Kanonische PidTagDisplayType-Eigenschaft](pidtagdisplaytype-canonical-property.md)
  
[PidTagEntryId (kanonische Eigenschaft)](pidtagentryid-canonical-property.md)
  
[Kanonische PidTagRecipientType-Eigenschaft](pidtagrecipienttype-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Verwalten des Arbeitsspeichers für ADRLIST- und SRowSet-Strukturen](managing-memory-for-adrlist-and-srowset-structures.md)

