---
title: IAddrBookAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c2546fc990169526361f2c452c50212123d8284d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407907"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt das Dialogfeld Outlook-Adressbuch an. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parameter

 _lpulUIParam_
  
> [in, out] Ein Zeiger auf einen Ziehpunkt des übergeordneten Fensters des Dialogfelds. Bei der Eingabe muss ein Fensterhandle immer übergeben werden. Wenn für die Ausgabe der **ulFlags** -Member des _lpAdrParms_ -Parameters auf DIALOG_SDI festgelegt ist, wird das Fensterhandle des nicht modalen Dialog Felds zurückgegeben. Weitere Informationen finden Sie in der "Anmerkungen". 
    
 _lpAdrParms_
  
> [in, out] Ein Zeiger auf eine [ADRPARM](adrparm.md) -Struktur, die die Darstellung und das Verhalten des Dialogfelds Adresse steuert. 
    
 _lppAdrList_
  
> [in, out] Ein Zeiger auf einen Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die Empfängerinformationen enthält. Bei der Eingabe kann dieser Parameter NULL sein oder auf einen gültigen Zeiger zeigen. Bei der Ausgabe zeigt dieser Parameter auf einen Zeiger auf gültige Empfängerinformationen. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Dialogfeld Allgemeine Adresse wurde erfolgreich angezeigt.
    
## <a name="remarks"></a>Bemerkungen

Wenn der **ulFlags** -Member des _lpAdrParms_ -Parameters auf DIALOG_SDI ist, der die Rückgabe des Fensterhandles des nicht modalen Dialog Felds bei der Ausgabe vorwegnimmt, wird es in Outlook ignoriert. die modale Version des Dialogs wird immer in nicht-Outlook-Clients angezeigt. 
  
Die **ADRLIST** -Struktur, die von MAPI an den Aufrufer über den Parameter _lppAdrList_ zurückgegeben wird, enthält ein Array von [Miet](adrentry.md) Strukturen, eine Struktur für jeden Empfänger. Bei Übergabe an die [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode einer ausgehenden Nachricht im _lpMods_ -Parameter kann die **ADRLIST** -Struktur zum Aktualisieren der Empfängerliste verwendet werden. 
  
Jede **Miet** Struktur in der **ADRLIST** -Struktur enthält NULL oder mehr [SPropValue](spropvalue.md) -Strukturen, eine Struktur für jeden Eigenschaftensatz für den Empfänger. Es kann keine **SPropValue** -Strukturen geben, wenn das von der **Address** -Methode vorgestellte Dialogfeld zum Entfernen eines Empfängers verwendet wird. Wenn es eine oder mehrere **SPropValue** -Strukturen gibt, wird die entsprechende **Miet** Struktur verwendet, um einen Empfänger hinzuzufügen oder zu aktualisieren. Der Empfänger kann aufgelöst werden, was darauf hinweist, dass eine der **SPropValue** -Strukturen die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft des Empfängers beschreibt oder nicht aufgelöst wird, was darauf hinweist, dass die **PR_ENTRYID** -Eigenschaft fehlt. 
  
Zusätzlich zu **PR_ENTRYID**sind aufgelöste Empfänger die folgenden Eigenschaften:
  
- **PR_RECIPIENT_TYPE** ([Pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Die **ADRLIST** -Struktur, die der Aufrufer übergibt, kann eine andere Größe als die von MAPI zurückgegebene Struktur aufweisen. Wenn MAPI eine größere **ADRLIST** -Struktur zurückgeben muss, gibt Sie die ursprüngliche Struktur frei und weist eine neue an. Wenn Sie Speicher für die **ADRLIST** -Struktur reservieren, ordnen Sie den Speicher für jede **SPropValue** -Struktur separat zu. Weitere Informationen zum Zuweisen und Freigeben von **ADRLIST** -Strukturen finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **Address** gibt sofort zurück, wenn das DIALOG_SDI-Flag im **ulFlags** -Element der **ADRPARM** -Struktur im _lpAdrParms_ -Parameter festgelegt ist. Das DIALOG_SDI-Flag wird für nicht-Outlook-Clients ignoriert. Wenn DIALOG_SDI ignoriert wird, wird die modale Version des Dialog Felds angezeigt, und ein Zeiger auf ein Handle sollte in _lpulUIParam_nicht erwartet werden.
  
 **Address** unterstützt Unicode-Zeichenfolgen in der **ADRPARM** -Struktur, wenn AB_UNICODEUI im **ulFlags** -Element von **ADRPARM** im _lpAdrParms_ -Parameter angegeben wurde und Unicode-Zeichenfolgen in ** ADRLIST**. Die Unicode-Zeichenfolgen werden in das Mehrbyte-Format (multibyte Character String) konvertiert, bevor Sie im Dialogfeld Outlook-Adressbuch angezeigt werden.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIStoreFunctions. cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI verwendet die **Address** -Methode, um dem Benutzer zu ermöglichen, das zu öffnende Postfach auszuwählen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[ADRPARM](adrparm.md)
  
[FreePadrlist](freepadrlist.md)
  
[FreeProws](freeprows.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

