---
title: IAddrBookAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1c4516c081fdd4cd41b1675a41d42957d6d4dd03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592473"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt das Dialogfeld Outlook Adressbuch an. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parameter

 _lpulUIParam_
  
> [in, out] Ein Zeiger auf ein Handle des übergeordneten Fensters des Dialogfelds. Bei der Eingabe muss immer ein Fensterhandle übergeben werden. Wenn der **ulFlags-Member** des  _lpAdrParms-Parameters_ bei der Ausgabe auf DIALOG_SDI festgelegt ist, wird das Fensterhandle des Dialogfelds ohne Modus zurückgegeben. Weitere Informationen finden Sie in der "Anmerkungen". 
    
 _lpAdrParms_
  
> [in, out] Ein Zeiger auf eine [ADRPARM-Struktur,](adrparm.md) die die Darstellung und das Verhalten des Adressdialogfelds steuert. 
    
 _lppAdrList_
  
> [in, out] Ein Zeiger auf einen Zeiger auf eine [ADRLIST-Struktur,](adrlist.md) die Empfängerinformationen enthält. Bei der Eingabe kann dieser Parameter NULL sein oder auf einen gültigen Zeiger zeigen. Bei der Ausgabe zeigt dieser Parameter auf einen Zeiger auf gültige Empfängerinformationen. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das allgemeine Adressdialogfeld wurde erfolgreich angezeigt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der **ulFlags-Member** des _LpAdrParms-Parameters_ auf DIALOG_SDI Vorwegnehmen der Rückgabe des Fensterhandle des Dialogfelds ohne Modus bei der Ausgabe festgelegt ist, wird es in Outlook ignoriert. Die modale Version des Dialogfelds wird immer in Nicht-Outlook Clients angezeigt. 
  
Die **ADRLIST-Struktur,** die von MAPI über den  _lppAdrList-Parameter_ an den Aufrufer zurückgegeben wird, enthält ein Array von [ADRENTRY-Strukturen,](adrentry.md) eine Struktur für jeden Empfänger. Wenn sie an die [IMessage::ModifyRecipients-Methode](imessage-modifyrecipients.md) einer ausgehenden Nachricht im  _lpMods-Parameter_ übergeben wird, kann die **ADRLIST-Struktur** verwendet werden, um die Empfängerliste zu aktualisieren. 
  
Jede **ADRENTRY-Struktur** in der **ADRLIST-Struktur** enthält null oder mehr [SPropValue-Strukturen,](spropvalue.md) eine Struktur für jeden Eigenschaftensatz für den Empfänger. Es kann keine **SPropValue-Strukturen** geben, wenn das von der **Address-Methode** angezeigte Dialogfeld zum Entfernen eines Empfängers verwendet wird. Wenn eine oder mehrere **SPropValue-Strukturen** vorhanden sind, wird die entsprechende **ADRENTRY-Struktur** verwendet, um einen Empfänger hinzuzufügen oder zu aktualisieren. Der Empfänger kann aufgelöst werden, was bedeutet, dass eine der **SPropValue-Strukturen** die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft des Empfängers beschreibt oder nicht aufgelöst ist, was darauf hinweist, dass die **PR_ENTRYID-Eigenschaft** fehlt. 
  
Zusätzlich zu **PR_ENTRYID** enthalten aufgelöste Empfänger die folgenden Eigenschaften:
  
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Die **ADRLIST-Struktur,** die der Aufrufer übergibt, kann eine andere Größe als die von der MAPI zurückgegebene Struktur aufweisen. Wenn die MAPI eine größere **ADRLIST-Struktur** zurückgeben muss, gibt sie die ursprüngliche Struktur frei und weist eine neue zu. Wenn Sie Speicher für die **ADRLIST-Struktur** zuordnen, weisen Sie den Speicher für jede **SPropValue-Struktur** separat zu. Weitere Informationen zum Zuordnen und Freigeben von **ADRLIST-Strukturen** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter. Das flag DIALOG_SDI wird für Nicht-Outlook-Clients ignoriert. Wenn DIALOG_SDI ignoriert wird, wird die modale Version des Dialogfelds angezeigt, und ein Zeiger auf ein Handle sollte in  _lpulUIParam_ nicht erwartet werden.
  
 **Address** unterstützt Unicode-Zeichenzeichenfolgen in der **ADRPARM-Struktur,** wenn AB_UNICODEUI im **ulFlags-Element** von **ADRPARM** im  _lpAdrParms-Parameter_ angegeben wurde, und unicode-Zeichenzeichenfolgen in **ADRLIST** unterstützt. Die Unicode-Zeichenfolgen werden in das MBCS-Format (Multibyte Character String) konvertiert, bevor sie im Dialogfeld Outlook Adressbuch angezeigt werden.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI verwendet die **Address-Methode,** damit der Benutzer auswählen kann, welches Postfach geöffnet werden soll.  <br/> |
   
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

