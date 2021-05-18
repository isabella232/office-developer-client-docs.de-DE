---
title: IABContainerResolveNames
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.ResolveNames
api_type:
- COM
ms.assetid: 27474af2-29a2-4cfb-b94f-72eb91562dac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fac4978bef94650f85ac3179acd3858602f933ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405814"
---
# <a name="iabcontainerresolvenames"></a>IABContainer::ResolveNames

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führt die Namensauflösung für einen oder mehrere Empfängereinträge aus.
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a>Parameter

 _lpPropTagArray_
  
> [in] Ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die die Eigenschaften beschreiben, die in der vom Anbieter zurückgegebenen [ADRLIST-Struktur](adrlist.md) enthalten sein sollen. Wenn Sie den Standardeigenschaftensatz des Anbieters anfordern, übergeben Sie NULL im _lpPropTagArray-Parameter._ 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Texttyp in den zurückgegebenen Zeichenfolgen steuert. Die folgenden Kennzeichen können festgelegt werden:
    
EMS_AB_ADDRESS_LOOKUP
  
> Es werden nur genaue Übereinstimmungen mit Proxyadressen gefunden. Teilweise Übereinstimmungen werden ignoriert. Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.
    
MAPI_CACHE_ONLY
  
> Nur das Offlineadressbuch wird zum Ausführen der Namensauflösung verwendet. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung das Öffnen der globalen Adressliste (GAL) im zwischengespeicherten Exchange-Modus und den Zugriff auf einen Eintrag in diesem Adressbuch aus dem Cache zu ermöglichen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt. 
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgeneigenschaften sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 _lpAdrList_
  
> [in, out] Bei der Eingabe ein Zeiger auf eine **ADRLIST-Struktur,** die die Liste der empfänger enthält, die aufgelöst werden sollen. Bei der Ausgabe ein Zeiger auf eine **ADRLIST-Struktur,** die die aufgelösten Namen enthält. 
    
 _lpFlagList_
  
> [in, out] Ein Zeiger auf ein Array von Flags, jedes Flag, das einer [ADRENTRY-Struktur](adrentry.md) im  _lpAdrList-Parameter_ entspricht und den Status des Namensauflösungsvorgangs für den Empfänger anfordert. Die Flags im  _lpFlagList-Parameter_ befinden sich in der gleichen Reihenfolge wie die Einträge in  _lpAdrList_. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_AMBIGUOUS 
  
> Der entsprechende Empfänger wurde aufgelöst, jedoch nicht in einen eindeutigen Eintragsbezeichner. Andere Container sollten nicht versuchen, diesen Empfänger zu beheben. 
    
MAPI_RESOLVED 
  
> Der entsprechende Empfänger wurde in einen eindeutigen Eintragsbezeichner aufgelöst. Andere Container sollten nicht versuchen, diesen Empfänger zu beheben. 
    
MAPI_UNRESOLVED 
  
> Der entsprechende Eintrag wurde nicht aufgelöst. Andere Container sollten versuchen, diesen Empfänger zu beheben.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Namensauflösungsprozess war erfolgreich.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Der Adressbuchanbieter unterstützt keine Massennamenauflösung mithilfe dieser Methode.
    
## <a name="remarks"></a>Hinweise

Die **ResolveNames-Methode** versucht, nicht aufgelösten Empfängern aus dem Array von Einträgen im  _lpAdrList-Parameter_ Empfängern in diesem Adressbuchcontainer zu entsprechen. Ein nicht aufgelöster Empfänger verfügt in der Regel **nur über PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft und möglicherweise einige andere Eigenschaften. Ein nicht aufgelöster Empfänger verfügt nicht über die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft, und das entsprechende Flag im  _lpFlagList-Parameter_ ist auf MAPI_UNRESOLVED. Umgekehrt verfügt ein aufgelöster Empfänger immer über mindestens die **PR_ENTRYID-Eigenschaft** sowie mehrere andere Eigenschaften wie **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME** und **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
Die Namensauflösung beginnt in der Regel, wenn ein Client die [IAddrBook::ResolveName-Methode](iaddrbook-resolvename.md) aufruft. Outlook MAPI antwortet, indem die **ResolveNames-Methode** jedes Adressbuchcontainers im Adressbuchsuchpfad, angegeben durch die **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) -Eigenschaft, aufruft. Die Einträge im  _lpAdrList-Parameter_ enthalten empfänger, die bereits aufgelöst wurden, da sie sich in Containern befinden, für die MAPI bereits **ResolveNames** aufgerufen hat, da die Einträge früher im Suchpfad angezeigt werden. 
  
Jeder Container versucht, die nicht aufgelösten Einträge zu beheben, indem er den Anzeigenamen des Empfängers mit dem Anzeigenamen eines seiner Einträge abgleicht. Wenn eine eindeutige Übereinstimmung gefunden wird, fügt **ResolveNames** die **PR_ENTRYID-Eigenschaft** und andere Eigenschaften, die im  _lpPropTagArray-Parameter_ enthalten sind, dem entsprechenden Eintrag in der ausgehenden **ADRLIST-Struktur** hinzu. **ResolveNames** legt dann den Eintrag im  _lpFlagList-Parameter_ auf MAPI_RESOLVED. Die in der PR_ENTRYID **gespeicherte** Eintrags-ID kann kurz- oder langfristig sein. 
  
Nachdem alle Container im Suchpfad versucht haben, den Namensauflösungsprozess zu starten, öffnet MAPI nach Möglichkeit ein Dialogfeld, in dem der Benutzer zur Lösung verbleibender Konflikte aufgefordert wird. 
  
Clients können die zurückgegebene **ADRLIST-Struktur** auch in Aufrufen der [IMessage::ModifyRecipients-Methode](imessage-modifyrecipients.md) verwenden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie müssen die Namensauflösung nicht mit der **ResolveNames-Methode** unterstützen. Stattdessen oder zusätzlich können Sie sie mit der PR_ANR **(** [PidTagAnr](pidtaganr-canonical-property.md)) -Eigenschaftseinschränkung unterstützen. Wenn Sie sich für die Namensauflösung auf **die PR_ANR** verlassen möchten, können Sie MAPI_E_NO_SUPPORT. For more information, see [Implementieren der Namensaufl�sung](implementing-name-resolution.md).
  
Legen Sie den Flageintrag eines Empfängers im  _lpFlagList-Parameter_ auf MAPI_UNRESOLVED, wenn der Empfänger keinem der Empfänger des Containers zu entsprechen hat. 
  
Wenn ein Empfänger mehreren Empfängern entspricht, legen Sie das Flag auf MAPI_AMBIGUOUS und ändern Sie die **ADRENTRY-Struktur nicht.** 
  
MAPI erfordert bestimmte Eigenschaften für Empfänger, die in der Empfängerliste einer Nachricht enthalten sind. Sie können sie in die **ADRENTRY-Struktur** als Teil des Namensauflösungsprozesses hinzufügen oder warten, bis MAPI sie mit Aufrufen der [Methoden IAddrBook::P repareRecips](iaddrbook-preparerecips.md) und [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) anfordert. Sie können diese zusätzlichen Aufrufe eliminieren und die Leistung verbessern, indem Sie die folgenden Eigenschaften in die **ADRENTRY-Strukturen** aller aufgelösten Empfänger einschl. 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Wenn einige eigenschaften im  _lpPropTagArray-Parameter_ nicht verfügbar sind – in der Regel, weil der Containereintrag die Eigenschaften nicht unterstützt und sie nicht im **ADRENTRY-Element** des Empfängers in der **ADRLIST-Struktur** enthalten sind – legen Sie den Eigenschaftentyp jeder nicht verfügbaren Eigenschaft auf PT_ERROR. 
  
Entfernen Sie keine Eigenschaften aus der **ADRENTRY-Struktur** eines aufgelösten Empfängers. 
  
Wenn Sie eine **ADRENTRY-Struktur** ersetzen und nicht ändern müssen, geben Sie zuerst die ursprüngliche **ADRENTRY-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen, und weisen Sie dann die alternative **ADRENTRY-Struktur** mit [MAPIAllocateBuffer](mapiallocatebuffer.md)zu.
  
## <a name="see-also"></a>Siehe auch



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[PidTagAnr (kanonische Eigenschaft)](pidtaganr-canonical-property.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

