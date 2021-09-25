---
title: IABContainerResolveNames
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABContainer.ResolveNames
api_type:
- COM
ms.assetid: 27474af2-29a2-4cfb-b94f-72eb91562dac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4430388382b867ece21209e48a7cc4b647df1674
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614045"
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
  
> [in] Ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftentags enthält, die die Eigenschaften beschreiben, die in der vom Anbieter zurückgegebenen [ADRLIST-Struktur](adrlist.md) enthalten sein sollen. Um den Standardsatz der Eigenschaften des Anbieters anzufordern, übergeben Sie NULL im _LpPropTagArray-Parameter._ 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Texttyp in den zurückgegebenen Zeichenfolgen steuert. Die folgenden Flags können festgelegt werden:
    
EMS_AB_ADDRESS_LOOKUP
  
> Es werden nur genaue Proxyadressenüberstimmungen gefunden. Partielle Übereinstimmungen werden ignoriert. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
MAPI_CACHE_ONLY
  
> Nur das Offlineadressbuch wird verwendet, um die Namensauflösung auszuführen. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung zu ermöglichen, die globale Adressliste (GAL) im Cache-Exchange-Modus zu öffnen und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt. 
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgeneigenschaften haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 _lpAdrList_
  
> [in, out] Bei der Eingabe ein Zeiger auf eine **ADRLIST-Struktur,** die die Liste der empfänger enthält, die aufgelöst werden sollen. Bei der Ausgabe ein Zeiger auf eine **ADRLIST-Struktur,** die die aufgelösten Namen enthält. 
    
 _lpFlagList_
  
> [in, out] Ein Zeiger auf ein Array von Flags, jedes Flag, das einer [ADRENTRY-Struktur](adrentry.md) im  _lpAdrList-Parameter_ entspricht und den Status des Namensauflösungsvorgangs für den Empfänger bereitstellt. Die Flags im  _lpFlagList_ -Parameter sind in der gleichen Reihenfolge wie die Einträge in  _lpAdrList_. Die folgenden Flags können festgelegt werden:
    
MAPI_AMBIGUOUS 
  
> Der entsprechende Empfänger wurde aufgelöst, jedoch nicht in einen eindeutigen Eintragsbezeichner. Andere Container sollten nicht versuchen, diesen Empfänger aufzulösen. 
    
MAPI_RESOLVED 
  
> Der entsprechende Empfänger wurde in einen eindeutigen Eintragsbezeichner aufgelöst. Andere Container sollten nicht versuchen, diesen Empfänger aufzulösen. 
    
MAPI_UNRESOLVED 
  
> Der entsprechende Eintrag wurde nicht aufgelöst. Andere Container sollten versuchen, diesen Empfänger aufzulösen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Vorgang zur Namensauflösung war erfolgreich.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Der Adressbuchanbieter unterstützt die Massennamenauflösung mit dieser Methode nicht.
    
## <a name="remarks"></a>Bemerkungen

Die **ResolveNames-Methode** versucht, nicht aufgelöste Empfänger aus dem Array von Einträgen im  _lpAdrList-Parameter_ an Empfänger in diesem Adressbuchcontainer zuzuordnen. Ein nicht aufgelöster Empfänger verfügt in der Regel nur über die **eigenschaft PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und möglicherweise über einige andere Eigenschaften. Ein nicht aufgelöster Empfänger verfügt nicht über die **Eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), und das entsprechende Flag im  _lpFlagList-Parameter_ ist auf MAPI_UNRESOLVED festgelegt. Umgekehrt weist ein aufgelöster Empfänger immer mindestens die **PR_ENTRYID-Eigenschaft** sowie mehrere andere Eigenschaften auf, z. **B. PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME** und **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
Die Namensauflösung beginnt in der Regel, wenn ein Client die [IAddrBook::ResolveName-Methode aufruft.](iaddrbook-resolvename.md) Outlook MAPI antwortet, indem die **ResolveNames-Methode** jedes Adressbuchcontainers aufgerufen wird, der im Adressbuchsuchpfad enthalten ist, der durch die **eigenschaft PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) angegeben wird. Die Einträge im  _lpAdrList-Parameter_ enthalten Empfänger, die bereits aufgelöst wurden, da sie sich in Containern befinden, für die MAPI **resolveNames** bereits aufgerufen hat, da die Einträge weiter oben im Suchpfad angezeigt werden. 
  
Jeder Container versucht, die nicht aufgelösten Einträge aufzulösen, indem der Anzeigename des Empfängers mit dem Anzeigenamen eines seiner Einträge übereinstimmt. Wenn eine eindeutige Übereinstimmung gefunden wird, fügt **ResolveNames** dem entsprechenden Eintrag in der ausgehenden **ADRLIST-Struktur** die **PR_ENTRYID eigenschaft** und andere Eigenschaften hinzu, die im _lpPropTagArray-Parameter_ enthalten sind. **ResolveNames** legt dann den Eintrag im  _parameter lpFlagList_ auf MAPI_RESOLVED fest. Der in der **PR_ENTRYID-Eigenschaft** gespeicherte Eintragsbezeichner kann kurz- oder langfristig sein. 
  
Nachdem alle Container im Suchpfad versucht haben, den Namensauflösungsprozess durchzuführen, öffnet MAPI nach Möglichkeit ein Dialogfeld, in dem der Benutzer um Hilfe bei der Lösung verbleibender Konflikte aufgefordert wird. 
  
Clients können die zurückgegebene **ADRLIST-Struktur** auch in Aufrufen der [IMessage::ModifyRecipients-Methode](imessage-modifyrecipients.md) verwenden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie müssen die Namensauflösung nicht mit der **ResolveNames-Methode** unterstützen. Stattdessen oder zusätzlich können Sie dies mit der Eigenschaftseinschränkung **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) unterstützen. Wenn Sie sich für die Namensauflösung auf die **PR_ANR** Einschränkung verlassen möchten, können Sie MAPI_E_NO_SUPPORT zurückgeben. For more information, see [Implementieren der Namensaufl�sung](implementing-name-resolution.md).
  
Legen Sie den Flageintrag eines Empfängers im  _parameter lpFlagList_ auf MAPI_UNRESOLVED fest, wenn der Empfänger keinem empfänger des Containers entspricht. 
  
Wenn ein Empfänger mehreren Empfängern entspricht, legen Sie das Kennzeichen auf MAPI_AMBIGUOUS fest, und ändern Sie die **ADRENTRY-Struktur** nicht. 
  
MAPI erfordert bestimmte Eigenschaften für Empfänger, die in der Empfängerliste einer Nachricht enthalten sind. Sie können sie in die **ADRENTRY-Struktur** als Teil des Namensauflösungsprozesses einschließen oder warten, bis MAPI sie mit Aufrufen der Methoden [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) und [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) anfordert. Sie können diese zusätzlichen Aufrufe vermeiden und die Leistung verbessern, indem Sie die folgenden Eigenschaften in die **ADRENTRY-Strukturen** aller aufgelösten Empfänger einschließen: 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Wenn einige eigenschaften im  _lpPropTagArray-Parameter_ nicht verfügbar sind – in der Regel, weil der Containereintrag die Eigenschaften nicht unterstützt und sie nicht im **ADRENTRY-Element** des Empfängers in der **ADRLIST-Struktur** enthalten sind – legen Sie den Eigenschaftentyp jeder nicht verfügbaren Eigenschaft auf PT_ERROR fest. 
  
Entfernen Sie keine Eigenschaften aus der **ADRENTRY-Struktur** eines aufgelösten Empfängers. 
  
Wenn Sie eine **ADRENTRY-Struktur** ersetzen müssen, geben Sie zuerst die ursprüngliche **ADRENTRY-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen, und weisen Sie dann die **Ersatz-ADRENTRY-Struktur** mit [MAPIAllocateBuffer](mapiallocatebuffer.md)zu.
  
## <a name="see-also"></a>Siehe auch



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Kanonische PidTagAnr-Eigenschaft](pidtaganr-canonical-property.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

