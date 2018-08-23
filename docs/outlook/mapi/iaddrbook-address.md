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
ms.openlocfilehash: a13696b355e6fd815cd6bda42843505d9fc3d1f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579956"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Zeigt das Dialogfeld Adressbuch von Outlook-Adresse an. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parameter

 _lpulUIParam_
  
> [in, out] Ein Zeiger auf ein Handle für das übergeordnete Fenster des Dialogfelds. Bei der Eingabe muss immer ein Fensterhandle übergeben werden. Wenn der **UlFlags** Member des Parameters _LpAdrParms_ auf DIALOG_SDI, festgelegt ist, wird bei der Ausgabe der Fensterhandle des modalen Dialogfelds zurückgegeben. Weitere Informationen finden Sie in der "Anmerkungen". 
    
 _lpAdrParms_
  
> [in, out] Ein Zeiger auf eine [ADRPARM](adrparm.md) -Struktur, die die Darstellung und das Verhalten des Dialogfelds Adresse steuert. 
    
 _lppAdrList_
  
> [in, out] Ein Zeiger auf einen Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die Empfängerinformationen enthält. Dieser Parameter kann bei der Eingabe NULL sein oder zeigen Sie auf einen gültigen Zeiger. Ausgabe zeigt dieser Parameter auf einen Zeiger auf gültige Empfängerinformationen. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Dialogfeld allgemeine Adresse wurde erfolgreich angezeigt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der **UlFlags** Member des Parameters _LpAdrParms_ vorhersehen von die Rückgabe von den Fensterhandle des modalen Dialogfelds auf Ausgabe DIALOG_SDI festgelegt ist, wird es in Outlook ignoriert. die modale Version des Dialogfelds wird immer in Outlook nicht angezeigt. 
  
Die **ADRLIST** -Struktur wird wieder von MAPI an dem Anrufer über den _LppAdrList_ -Parameter übergeben enthält ein Array von [ADRENTRY](adrentry.md) -Strukturen, eine Struktur für jeden Empfänger. Wenn Sie eine ausgehende Nachricht [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode in der _LpMods_ -Parameter übergeben wird, kann die **ADRLIST** -Struktur so aktualisieren Sie die Empfängerliste verwendet werden. 
  
Jede **ADRENTRY** Struktur in der Struktur **ADRLIST** enthält null oder mehr [SPropValue](spropvalue.md) Strukturen, eine Struktur für jede Eigenschaft, die für den Empfänger festgelegt. Wenn das Dialogfeld präsentiert von der **Adresse** -Methode verwendet wird, um einen Empfänger zu entfernen kann 0 (null) **SPropValue** Strukturen sein. Wenn ein oder mehrere **SPropValue** Strukturen vorhanden sind, wird die entsprechende **ADRENTRY** -Struktur hinzufügen oder aktualisieren einen Empfänger verwendet. Der Empfänger kann nicht aufgelöst werden gibt an, dass eine der Strukturen **SPropValue** des Empfängers **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft beschreibt oder nicht aufgelöst, was bedeutet, dass die **PR_ENTRYID** -Eigenschaft ist, ist nicht vorhanden. 
  
Zusätzlich zur **PR_ENTRYID**gehören aufgelösten Empfänger die folgenden Eigenschaften:
  
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Die **ADRLIST** -Struktur, der der Anrufer übergibt möglicherweise eine andere Größe aus der Struktur, die MAPI zurückgibt. Wenn MAPI eine größere **ADRLIST** Struktur zurückgeben muss, Originalstruktur frei und ordnet einen neuen Anwendungspool. Wenn Sie Speicher für die **ADRLIST** -Struktur reservieren, weisen Sie des Speichers separat für jedes **SPropValue** Struktur. Weitere Informationen zum Zuordnen und Freigeben von **ADRLIST** -Strukturen finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **Adresse** wird sofort zurückgegeben, wenn das Flag DIALOG_SDI im **UlFlags** -Member der Struktur **ADRPARM** im _LpAdrParms_ -Parameter festgelegt ist. Das Flag DIALOG_SDI für nicht-Outlook-Clients ignoriert. DIALOG_SDI ignoriert wird, wird die modale Version des Dialogfelds angezeigt werden und ein Zeiger auf ein Handle sollte nicht in _LpulUIParam_erwartet werden.
  
 **Adresse** unterstützt Unicode-Zeichenfolgen in der Struktur **ADRPARM** , wenn AB_UNICODEUI im **UlFlags** -Member **ADRPARM** im _LpAdrParms_ -Parameter angegeben wurde, und es Unicode-Zeichenfolgen in **unterstützt ADRLIST**. Die Unicode-Zeichenfolgen werden in der multibyte-Zeichenfolge handeln Zeichenformat konvertiert, bevor sie im Dialogfeld Outlook-Adresse Adressbuch angezeigt werden.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI (engl.) verwendet die **Adresse** -Methode, um die Benutzer welches Postfach zum Öffnen auswählen kann.  <br/> |
   
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


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

