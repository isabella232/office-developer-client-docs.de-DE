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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cb683178a8e258f571cbc3d05a3b030481905433
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792345"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**Betrifft**: Outlook 
  
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
  
> [in, out] Ein Zeiger auf das Handle des übergeordneten Fensters des Dialogfelds. Bei der Eingabe muss immer ein Fensterhandle übergeben werden. Wenn das Flag DIALOG_SDI in der [ADRPARM](adrparm.md) -Struktur, die auf das durch den Parameter _LpAdrParms_ festgelegt ist, wird bei der Ausgabe der Fensterhandle des modalen Dialogfelds zurückgegeben. 
    
 _lpAdrParms_
  
> [in, out] Ein Zeiger auf eine **ADRPARM** -Struktur, die die Darstellung und das Verhalten des Dialogfelds Adresse steuert. 
    
 _lppAdrList_
  
> [in, out] Ein Zeiger auf einen Zeiger auf eine Adressliste. Bei der Eingabe diese Liste ist entweder die aktuelle Liste der Empfänger in einer Nachricht oder NULL, wenn die Liste nicht vorhanden ist. Ausgabe _LppAdrList_ zeigt auf eine aktualisierte Liste der Empfänger der Nachricht. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Dialogfeld Adresse wurde erfolgreich angezeigt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::Address** -Methode wird für Address Book Anbieter Unterstützungsobjekte implementiert. Von adressbuchanbietern implementierte Aufrufen **Adresse** zum Erstellen oder aktualisieren eine Liste der Empfänger der Nachricht. 
  
Jeden Empfänger wird in eine Struktur [ADRENTRY](adrentry.md) beschrieben, die in der [ADRLIST](adrlist.md) -Struktur, die auf das durch den Parameter _LppAdrList_ enthalten ist. Die **ADRENTRY** -Datenstruktur enthält ein Array von Eigenschaftswerten Empfänger, von denen des Empfängers Typ oder **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))-Eigenschaft ist. Diese Struktur **ADRLIST** kann an einen Client für die Verwendung als _LpMods_ -Parameter in einem Aufruf von [IMessage::ModifyRecipients](imessage-modifyrecipients.md)übergeben werden.
  
Jeden Empfänger in der Struktur **ADRLIST** kann entweder aufgelöst werden gibt an, dass eine Eigenschaftswerte dessen **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft ist oder nicht aufgelöst ist, gibt an, dass die Eigenschaft **PR_ENTRYID** ist, ist nicht vorhanden. 
  
Zusätzlich zur **PR_ENTRYID**gehören aufgelösten Empfänger die folgenden Eigenschaften:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Nicht aufgelösten Empfänger beinhalten in der Regel nur **PR_DISPLAY_NAME** und **PR_RECIPIENT_TYPE**. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **ADRLIST** -Struktur, der der Anrufer übergibt möglicherweise eine andere Größe aus der Struktur, die MAPI zurückgibt. Wenn Sie Speicher für die **ADRLIST** -Struktur reservieren, weisen Sie des Speichers separat für jedes [SPropValue](spropvalue.md) Struktur. 
  
Verwenden Sie die Verweise auf die MAPI-Speicherverwaltungsfunktionen zu Ihrer [ABProviderInit](abproviderinit.md) -Funktion übergebene Arbeitsspeicher zugewiesen werden. Reservieren Sie Speicher mit der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) für **ADRLIST** und jede Eigenschaft Wert Struktur in den **ADRENTRY** Strukturen in **ADRLIST**. 
  
Wenn **Adresse** eine größere **ADRLIST** Struktur zurückgeben muss, oder wenn Sie NULL für _LppAdrList_übergeben haben, **Adresse** Originalstruktur frei und ordnet einen neuen Anwendungspool. **Adresse** auch zusätzliche Eigenschaft Wert Strukturen in der Struktur **ADRLIST** reserviert und alten entsprechend frei. Weitere Informationen zur Verwaltung des Arbeitsspeichers für **ADRLIST** Strukturen finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md).
  
 **Adresse** zurückgegeben sofort, wenn das Flag DIALOG_SDI in der Struktur **ADRPARM** im _LpAdrParms_ -Parameter festgelegt wurde. 
  
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
  
[Kanonische PidTagAddressType-Eigenschaft](pidtagaddresstype-canonical-property.md)
  
[Kanonische PidTagDisplayName-Eigenschaft](pidtagdisplayname-canonical-property.md)
  
[Kanonische PidTagDisplayType-Eigenschaft](pidtagdisplaytype-canonical-property.md)
  
[Kanonische-Eigenschaft PidTagEntryId](pidtagentryid-canonical-property.md)
  
[Kanonische PidTagRecipientType-Eigenschaft](pidtagrecipienttype-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[' Srowset '](srowset.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md)

