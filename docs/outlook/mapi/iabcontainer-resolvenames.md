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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279570"
---
# <a name="iabcontainerresolvenames"></a>IABContainer::ResolveNames

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führt die Namensauflösung für einen oder mehrere Empfänger Einträge aus.
  
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
  
> in Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags enthält, die die Eigenschaften beschreiben, die in die vom Anbieter zurückgegebene [ADRLIST](adrlist.md) -Struktur eingeschlossen werden sollen. Um den Standardsatz von Eigenschaften des Anbieters anzufordern, übergeben Sie NULL im _lpPropTagArray_ -Parameter. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Texttyp in den zurückgegebenen Zeichenfolgen steuert. Die folgenden Flags können festgelegt werden:
    
EMS_AB_ADDRESS_LOOKUP
  
> Nur genaue Proxyadressen Übereinstimmungen werden gefunden; partielle Übereinstimmungen werden ignoriert. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    
MAPI_CACHE_ONLY
  
> Nur das Offlineadressbuch wird zur Durchführung der Namensauflösung verwendet. Sie können dieses Flag beispielsweise verwenden, um eine Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus zu aktivieren und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt. 
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgeneigenschaften sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
 _lpAdrList_
  
> [in, out] Bei der Eingabe ein Zeiger auf eine **ADRLIST** -Struktur, die die Liste der zu lösenden Empfänger enthält. Bei der Ausgabe ein Zeiger auf eine **ADRLIST** -Struktur, die die aufgelösten Namen enthält. 
    
 _lpFlagList_
  
> [in, out] Ein Zeiger auf ein Array von Flags, jedes Flag, das einer [](adrentry.md) anmietungs Struktur im _lpAdrList_ -Parameter entspricht, die den Status der Namensauflösung für den Empfänger bereitstellt. Die Flags im _lpFlagList_ -Parameter befinden sich in der gleichen Reihenfolge wie die Einträge in _lpAdrList_. Die folgenden Flags können festgelegt werden:
    
MAPI_AMBIGUOUS 
  
> Der entsprechende Empfänger wurde aufgelöst, jedoch nicht zu einer eindeutigen Eintrags-ID. Andere Container sollten nicht versuchen, diesen Empfänger aufzulösen. 
    
MAPI_RESOLVED 
  
> Der entsprechende Empfänger wurde in eine eindeutige Eintrags-ID aufgelöst. Andere Container sollten nicht versuchen, diesen Empfänger aufzulösen. 
    
MAPI_UNRESOLVED 
  
> Der entsprechende Eintrag wurde nicht aufgelöst. Andere Container sollten versuchen, diesen Empfänger aufzulösen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Prozess der Namensauflösung war erfolgreich.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Der Adressbuchanbieter unterstützt die Auflösung von Massen Namen nicht mithilfe dieser Methode.
    
## <a name="remarks"></a>Bemerkungen

Die **ResolveNames** -Methode versucht, nicht aufgelöste Empfänger aus dem Array der Einträge im _lpAdrList_ -Parameter an Empfänger in diesem Adressbuchcontainer anzupassen. Ein nicht aufgelöster Empfänger hat in der Regel nur die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft und möglicherweise einige andere Eigenschaften. Ein nicht aufgelöster Empfänger verfügt nicht über die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft, und das entsprechende Flag im _LPFLAGLIST_ -Parameter ist auf MAPI_UNRESOLVED festgelegt. Umgekehrt hat ein aufgelöster Empfänger immer mindestens die **PR_ENTRYID** -Eigenschaft und mehrere andere Eigenschaften wie **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**und **PR_ADDRTYPE** ([ Pidtagaddresstype (](pidtagaddresstype-canonical-property.md)).
  
Die Namensauflösung wird in der Regel gestartet, wenn ein Client die [IAddrBook::](iaddrbook-resolvename.md) ResolveName-Methode aufruft. Outlook MAPI antwortet durch Aufrufen der **ResolveNames** -Methode jedes Adressbuch Containers, der im Adressbuch Suchpfad enthalten ist, angegeben durch die **PR_AB_SEARCH_PATH** ([pidtagabsearchpath (](pidtagabsearchpath-canonical-property.md))-Eigenschaft. Die Einträge im _lpAdrList_ -Parameter enthalten bereits aufgelöste Empfänger, da Sie sich in Containern befinden, für die MAPI bereits **ResolveNames**aufgerufen hat, da die Einträge weiter oben im Suchpfad angezeigt werden. 
  
Jeder Container versucht, die nicht aufgelösten Einträge aufzulösen, indem der Anzeigename des Empfängers mit dem Anzeigenamen eines seiner Einträge abgeglichen wird. Wenn eine eindeutige Übereinstimmung gefunden wird, fügt **ResolveNames** die **PR_ENTRYID** -Eigenschaft und andere Eigenschaften, die im _lpPropTagArray_ -Parameter enthalten sind, dem entsprechenden Eintrag in der ausgehenden **ADRLIST** -Struktur hinzu. **ResolveNames** legt dann den Eintrag im _lpFlagList_ -Parameter auf MAPI_RESOLVED fest. Die in der **PR_ENTRYID** -Eigenschaft gespeicherte Eintrags-ID kann kurzfristig oder langfristig sein. 
  
Nachdem alle Container im Suchpfad den Prozess der Namensauflösung versucht haben, öffnet MAPI ein Dialogfeld, um den Benutzer aufzufordern, Hilfe beim Beheben von verbleibenden Konflikten zu erhalten. 
  
Clients können die zurückgegebene **ADRLIST** -Struktur auch in Aufrufen der [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode verwenden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie müssen die Namensauflösung nicht mit der **ResolveNames** -Methode unterstützen. Stattdessen oder zusätzlich können Sie diese mit der **PR_ANR** ([pidtaganr (](pidtaganr-canonical-property.md))-Eigenschaftseinschränkung unterstützen. Wenn Sie sich dafür entscheiden, die **PR_ANR** -Einschränkung für die Namensauflösung zu verwenden, können Sie MAPI_E_NO_SUPPORT zurückgeben. For more information, see [Implementieren der Namensaufl�sung](implementing-name-resolution.md).
  
Legen Sie den Flag-Eintrag eines Empfängers im _lpFlagList_ -Parameter auf MAPI_UNRESOLVED fest, wenn der Empfänger keinem der Empfänger des Containers entspricht. 
  
Wenn ein Empfänger mit mehreren Empfängern übereinstimmt, legen Sie sein Flag auf MAPI_AMBIGUOUS, und ändern Sie die zugehörige **Miet** Struktur nicht. 
  
MAPI erfordert bestimmte Eigenschaften für Empfänger, die in der Empfängerliste einer Nachricht enthalten sind. Sie können Sie als Teil des Namens Auflösungsprozesses in die **Miet** Struktur aufnehmen oder warten, bis MAPI Sie mit Aufrufen der Methoden [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) und [IMAPISupport:: ExpandRecips](imapisupport-expandrecips.md) anfordert. Sie können diese zusätzlichen Anrufe beseitigen und die Leistung verbessern, indem Sie die folgenden Eigenschaften in die **Miet** Strukturen aller aufgelösten Empfänger einbeziehen: 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY** ([Pidtagsearchkey (](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([Pidtagtransmittabledisplayname (](pidtagtransmittabledisplayname-canonical-property.md))
    
Wenn einige der Eigenschaften im _lpPropTagArray_ -Parameter nicht verfügbar sind (in der Regel, da der Container Eintrag die Eigenschaften nicht unterstützt und Sie nicht in der **ADRLIST** - **** Struktur des Empfängers enthalten sind) Legen Sie den Eigenschaftentyp jeder nicht verfügbaren Eigenschaft auf PT_ERROR. 
  
Entfernen Sie keine Eigenschaften aus der **Miet** Struktur eines aufgelösten Empfängers. 
  
Wenn Sie eine **Miet** Struktur ersetzen und nicht ändern müssen, können Sie zuerst die ursprüngliche **Miet** Struktur freigeben, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen und dann die Ersatz- **Miet** Struktur mit [ MAPIAllocateBuffer](mapiallocatebuffer.md).
  
## <a name="see-also"></a>Siehe auch



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Kanonische Pidtaganr (-Eigenschaft](pidtaganr-canonical-property.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

