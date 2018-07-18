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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ed87a2a6e3232cec492da6be032cf54cd66c3772
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791964"
---
# <a name="iabcontainerresolvenames"></a>IABContainer::ResolveNames

  
  
**Betrifft**: Outlook 
  
Führt die Auflösung für einen oder mehrere Empfänger Einträge.
  
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
  
> [in] Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags, beschreibt die Eigenschaften, die vom Anbieter zurückgegebenen [ADRLIST](adrlist.md) -Struktur enthält. Um die Standardeigenschaften des Anbieters anzufordern, übergeben Sie NULL in der _LpPropTagArray_ -Parameter. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ des Texts in der zurückgegebenen Zeichenfolge steuert. Die folgenden Kennzeichen können festgelegt werden:
    
EMS_AB_ADDRESS_LOOKUP
  
> Nur genauen Proxy Adresse Übereinstimmungen werden gefunden werden. teilweise übereinstimmenden werden ignoriert. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
MAPI_CACHE_ONLY
  
> Nur das Offlineadressbuch wird zum Ausführen von namensauflösung verwendet werden. Dieses Kennzeichen können Sie beispielsweise Hilfe eine Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt. 
    
PARAMETER MAPI_UNICODE 
  
> Die zurückgegebene Zeichenfolgeneigenschaften sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 _lpAdrList_
  
> [in, out] Bei der Eingabe einen Zeiger auf eine **ADRLIST** -Struktur, die enthält die Liste der Empfänger aufgelöst werden. Bei der Ausgabe einen Zeiger auf eine **ADRLIST** -Struktur, die aufgelösten Namen enthält. 
    
 _lpFlagList_
  
> [in, out] Ein Zeiger auf ein Array von Flags, enthält jedes Flag auf eine [ADRENTRY](adrentry.md) -Struktur in den _LpAdrList_ -Parameter entspricht, die den Status des Vorgangs Lösung Name für den Empfänger. Die Flags in der _LpFlagList_ -Parameter werden in der gleichen Reihenfolge in _LpAdrList_als Einträge. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_AMBIGUOUS 
  
> Der entsprechende Empfänger aufgelöst wurde, jedoch nicht für einen Eintrag Eindeutiger Bezeichner. Andere Container sollte nicht an diesen Empfänger zu beheben versuchen. 
    
MAPI_RESOLVED 
  
> Der entsprechende Empfänger wurde eine eindeutige Bezeichner behoben. Andere Container sollte nicht an diesen Empfänger zu beheben versuchen. 
    
MAPI_UNRESOLVED 
  
> Der entsprechende Eintrag wurde nicht behoben. Andere Container sollte versuchen, diese Empfänger aufzulösen.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Vorgang der Lösung war erfolgreich.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Der Adressbuchanbieter unterstützt keine namensauflösung Massen mithilfe dieser Methode.
    
## <a name="remarks"></a>Bemerkungen

Die **ResolveNames** -Methode versucht, nicht aufgelösten Empfänger aus dem Array der Einträge in der _LpAdrList_ -Parameter an Empfänger in dieser Adressbuchcontainer zuzuordnen. Ein nicht aufgelöster Empfänger hat in der Regel nur die Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und möglicherweise einigen andere Eigenschaften. Ein nicht aufgelöster Empfänger verfügt nicht über die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft, und die entsprechenden Flag im Parameter _LpFlagList_ auf MAPI_UNRESOLVED festgelegt ist. Umgekehrt wurde ein aufgelöster Empfänger immer mindestens die **PR_ENTRYID** -Eigenschaft sowie einige andere Eigenschaften wie **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**und **PR_ADDRTYPE** ([ PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
Namensauflösung beginnt in der Regel auf, wenn ein Client die [IAddrBook::ResolveName](iaddrbook-resolvename.md) -Methode aufruft. Outlook MAPI antwortet durch Aufrufen der Methode **ResolveNames** jedes Adressbuchcontainer enthalten im Address Book Suchpfad, durch die **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))-Eigenschaft angegeben. Die Einträge in der _LpAdrList_ -Parameter enthalten Empfänger bereits aufgelöst werden, da sie in Containern, die für die MAPI **ResolveNames**, bereits aufgerufen wurde sind, da die Einträge weiter oben in der Suchpfad angezeigt werden. 
  
Jeden Container versucht, die nicht aufgelösten Einträge aufzulösen, durch den Anzeigenamen des Empfängers mit dem Anzeigenamen eines der zugehörigen Einträge abgleichen. Wenn eine eindeutige Übereinstimmung gefunden wird, fügt **ResolveNames** die **PR_ENTRYID** -Eigenschaft und andere Eigenschaften, die im Parameter _LpPropTagArray_ für den entsprechenden Eintrag in der ausgehenden **ADRLIST** -Struktur enthalten sind. Klicken Sie dann der **ResolveNames** Eintrag im Parameter _LpFlagList_ für MAPI_RESOLVED festgelegt. Die Eintrags-ID in der Eigenschaft **PR_ENTRYID** gespeicherten möglich kurzfristige oder langfristige. 
  
Nachdem alle der Container in der Suche Pfad haben versucht Vorgang der Lösung, MAPI öffnet ein Dialogfeld, wenn möglich, um den Benutzer Hilfe zum Lösen von Konflikten verbleibenden aufzufordern. 
  
Clients können auch die zurückgegebene **ADRLIST** -Struktur in Aufrufe der [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode verwenden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie sind nicht erforderlich, zur Unterstützung von namensauflösung mit der **ResolveNames** -Methode. Stattdessen oder darüber hinaus können Sie es mit der eigenschaftseinschränkung **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) unterstützen. Wenn Sie sich entscheiden, auf die Einschränkung **PR_ANR** für namensauflösung verlassen, können Sie MAPI_E_NO_SUPPORT zurückgeben. For more information, see [Implementieren der Namensaufl�sung](implementing-name-resolution.md).
  
Legen Sie einen Empfänger Flag Eintrag im Parameter _LpFlagList_ für MAPI_UNRESOLVED, wenn der Empfänger nicht der Empfänger des Containers übereinstimmt. 
  
Wenn ein Empfänger mehrere Empfänger übereinstimmt, legen Sie dessen Flag auf MAPI_AMBIGUOUS und ändern Sie die Struktur **ADRENTRY** nicht. 
  
MAPI erfordert bestimmte Eigenschaften für den Empfänger an, die in der Liste der Empfänger einer Nachricht enthalten sind. Sie können in der Struktur **ADRENTRY** einbinden, im Rahmen des Prozesses Lösung Name oder warten MAPI, um sie mit der Aufrufe der Methoden [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) und [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) anfordern. Sie können diese zusätzlichen Aufrufe vermeiden und Verbessern der Leistung durch die folgenden Eigenschaften in die Strukturen **ADRENTRY** aller aufgelösten Empfänger einschließlich: 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Wenn einige der Eigenschaften im _LpPropTagArray_ -Parameter nicht verfügbar sind – in der Regel, da der Container-Eintrag nicht unterstützt, und sie die Eigenschaften sind nicht enthalten in der Aufgabenliste des Empfängers **ADRENTRY** Member in der Struktur **ADRLIST** – Legen Sie den Eigenschaftstyp der einzelnen nicht verfügbar-Eigenschaft auf PT_ERROR. 
  
Entfernen Sie alle Eigenschaften nicht aus einer aufgelösten Empfänger **ADRENTRY** Struktur. 
  
Wenn Sie müssen ersetzen, anstatt eine **ADRENTRY** -Struktur zu ändern, die ursprüngliche **ADRENTRY** Struktur zuerst durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion frei, und fügen dann die Ersetzung **ADRENTRY** Struktur mit [ MAPIAllocateBuffer](mapiallocatebuffer.md).
  
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

