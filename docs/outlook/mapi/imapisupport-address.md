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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331605"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt das Dialogfeld Allgemeine Adresse an. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parameter

 _lpulUIParam_
  
> [in, out] Ein Zeiger auf das Handle des übergeordneten Fensters des Dialogfelds. Bei der Eingabe muss ein Fensterhandle immer übergeben werden. Wenn das DIALOG_SDI-Flag in der [ADRPARM](adrparm.md) -Struktur festgelegt ist, auf die durch den _lpAdrParms_ -Parameter verwiesen wird, wird das Fensterhandle des Dialog Felds ohne Modus zurückgegeben. 
    
 _lpAdrParms_
  
> [in, out] Ein Zeiger auf eine **ADRPARM** -Struktur, die die Darstellung und das Verhalten des Dialogfelds Adresse steuert. 
    
 _lppAdrList_
  
> [in, out] Ein Zeiger auf einen Zeiger auf eine Adressliste. Bei der Eingabe ist diese Liste entweder die aktuelle Liste der Empfänger in einer Nachricht oder NULL, wenn keine solche Liste vorhanden ist. Bei der Ausgabe zeigt _lppAdrList_ auf eine aktualisierte Liste der Nachrichtenempfänger. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Dialogfeld Adresse wurde erfolgreich angezeigt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: Address** -Methode wird für Support Objekte des Adressbuch Anbieters implementiert. Adressbuchanbieter rufen die **Adresse** auf, um eine Liste der Nachrichtenempfänger zu erstellen oder zu aktualisieren. 
  
Jeder Empfänger wird in einer [Miet](adrentry.md) Struktur beschrieben, die in der [ADRLIST](adrlist.md) -Struktur enthalten ist, auf die durch den _lppAdrList_ -Parameter verwiesen wird. Die **Miet** Struktur enthält ein Array von Empfänger Eigenschaftswerten, von denen einer der Empfängertyp oder die **PR_RECIPIENT_TYPE** ([pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))-Eigenschaft ist. Diese **ADRLIST** -Struktur kann an einen Client übergeben werden, der als _lpMods_ -Parameter in einem Aufruf von [IMessage:: ModifyRecipients](imessage-modifyrecipients.md)verwendet wird.
  
Jeder Empfänger in der **ADRLIST** -Struktur kann aufgelöst werden, was darauf hinweist, dass einer seiner Eigenschaftswerte die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft oder nicht aufgelöst ist, was darauf hinweist, dass die **PR_ENTRYID** -Eigenschaft fehlt. 
  
Zusätzlich zu **PR_ENTRYID**sind aufgelöste Empfänger die folgenden Eigenschaften:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Nicht aufgelöste Empfänger schließen in der Regel nur **PR_DISPLAY_NAME** und **PR_RECIPIENT_TYPE**ein. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **ADRLIST** -Struktur, die der Aufrufer übergibt, kann eine andere Größe als die von MAPI zurückgegebene Struktur aufweisen. Wenn Sie Speicher für die **ADRLIST** -Struktur reservieren, ordnen Sie den Speicher für jede [SPropValue](spropvalue.md) -Struktur separat zu. 
  
Verwenden Sie die Zeiger auf die MAPI-Speicher Zuweisungsfunktionen, die an Ihre [ABProviderInit](abproviderinit.md) -Funktion übergeben werden, um Arbeitsspeicher zuzuweisen. Reservieren Sie Arbeitsspeicher mit der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion für **ADRLIST** und jeder Eigenschaftswert Struktur in den **Miet** Strukturen in **ADRLIST**. 
  
Wenn **Address** eine größere **ADRLIST** -Struktur zurückgeben muss oder wenn Sie NULL für _lppAdrList_übergeben haben, gibt **Address** die ursprüngliche Struktur frei und ordnet eine neue an. **Address** ordnet auch zusätzliche Eigenschaftswert Strukturen in der **ADRLIST** -Struktur zu und gibt alte nach Bedarf frei. Weitere Informationen zur Verwaltung von Arbeitsspeicher für **ADRLIST** -Strukturen finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
 **Address** gibt sofort zurück, wenn das DIALOG_SDI-Flag in der **ADRPARM** -Struktur im _lpAdrParms_ -Parameter festgelegt wurde. 
  
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
  
[Kanonische Pidtagaddresstype (-Eigenschaft](pidtagaddresstype-canonical-property.md)
  
[Kanonische PidTagDisplayName-Eigenschaft](pidtagdisplayname-canonical-property.md)
  
[Kanonische PidTagDisplayType-Eigenschaft](pidtagdisplaytype-canonical-property.md)
  
[Kanonische PidTagEntryId-Eigenschaft](pidtagentryid-canonical-property.md)
  
[Kanonische Pidtagrecipienttype (-Eigenschaft](pidtagrecipienttype-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Verwalten von Speicher für ADRLIST-und SRowSet-Strukturen](managing-memory-for-adrlist-and-srowset-structures.md)

