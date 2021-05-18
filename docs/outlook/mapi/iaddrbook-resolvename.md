---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8a6a73153b857078cb37d94a634a6b0215a0a8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408131"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führt die Namensauflösung durch und weist Empfängern in einer Empfängerliste Eintragsbezeichner zu.
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster eines Dialogfelds, das angezeigt wird, falls angegeben, um den Benutzer zur Lösung von Mehrdeutigkeiten aufforderen.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die verschiedene Aspekte des Auflösungsprozesses steuern. Die folgenden Kennzeichen können festgelegt werden:
    
AB_UNICODEUI
  
> Gibt an,  _dass lpszNewEntryTitle eine_ UNICODE-Zeichenfolge ist. 
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung zu ermöglichen, die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und aus dem Cache auf einen Eintrag in diesem Adressbuch zu zugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.
    
MAPI_DIALOG 
  
> Zeigt ein Dialogfeld an, in dem der Benutzer weitere Informationen zur Namensauflösung einfordert. Wenn dieses Kennzeichen nicht festgelegt ist, wird kein Dialogfeld angezeigt. 
    
MAPI_UNICODE 
  
> Gibt an, dass die in der Adressliste zurückgegebenen Eigenschaften vom Typ PT_UNICODE anstatt PT_STRING8. 
    
 _lpszNewEntryTitle_
  
> [in] Ein Zeiger auf Text für den Titel des Steuerelements im Dialogfeld, mit dem der Benutzer zur Eingabe eines Empfängers aufgefordert wird. Der Titel variiert je nach Empfängertyp. Der  _lpszNewEntryTitle-Parameter_ kann NULL sein. 
    
 _lpAdrList_
  
> [in-out] Ein Zeiger auf eine [ADRLIST-Struktur,](adrlist.md) die die Liste der empfängernamen enthält, die aufgelöst werden sollen. Diese **ADRLIST-Struktur** kann mit der [IAddrBook::Address-Methode erstellt](iaddrbook-address.md) werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Namensauflösungsprozess ist erfolgreich.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> Mindestens ein Empfänger im  _lpAdrList-Parameter_ hat mehreren Eintrag im Adressbuch entsprechen. In der Regel wird dieser Wert zurückgegeben, wenn MAPI_DIALOG festgelegt ist, was die Anzeige eines Dialogfelds verhindert. 
    
MAPI_E_NOT_FOUND 
  
> Mindestens ein Empfänger im  _lpAdrList-Parameter_ kann nicht aufgelöst werden. In der Regel wird dieser Wert zurückgegeben, wenn MAPI_DIALOG festgelegt ist, was die Anzeige eines Dialogfelds verhindert. 
    
## <a name="remarks"></a>Hinweise

Clients und Dienstanbieter rufen die **ResolveName-Methode** auf, um den Namensauflösungsprozess zu initiieren. Ein nicht aufgelöster Eintrag ist ein Eintrag, der noch keinen Eintragsbezeichner oder keine **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft hat.
  
 **ResolveName** durchgeht den folgenden Prozess für jeden nicht aufgelösten Eintrag in der Adressliste, der im  _lpAdrList-Parameter übergeben_ wird. 
  
1. Wenn der Adresstyp des Empfängers dem Format einer SMTP-Adresse ( _Anzeigename_ @  _domain.top-level-domain)_ zuzuordnen ist, weist **ResolveName** ihm eine eindeutige Eintrags-ID zu. 
    
2. Für jeden Container in der **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) -Eigenschaft ruft **ResolveName** die [IABContainer::ResolveNames-Methode](iabcontainer-resolvenames.md) auf. **ResolveNames** versucht, dem Anzeigenamen jedes nicht aufgelösten Empfängers einen Anzeigenamen zu geben, der zu einem seiner Einträge gehört. 
    
3. Wenn ein Container **ResolveNames** nicht unterstützt, **schränkt ResolveName** die Inhaltstabelle des Containers mithilfe einer **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) -Eigenschaftseinschränkung ein. Diese Einschränkung bewirkt, dass der Container eine "best guess"-Suchart zum Suchen eines übereinstimmenden Empfängers durch führt. Alle Container müssen die Einschränkung der **PR_ANR** unterstützen. 
    
4. Wenn ein Container einen Empfänger zurückgibt, der mehreren Namen entspricht, zeigt **ResolveName** ein Dialogfeld an, wenn das flag MAPI_DIALOG festgelegt ist, wodurch der Benutzer den richtigen Namen auswählen kann. 
    
5. Wenn alle Container in der PR_AB_SEARCH_PATH **aufgerufen** wurden und keine Übereinstimmung gefunden wurde, bleibt der Empfänger ungelöst. 
    
Wenn ein oder mehrere Empfänger nicht aufgelöst werden, gibt **ResolveName** MAPI_E_NOT_FOUND. Wenn ein oder mehrere Empfänger eine mehrdeutige Auflösung hatten, die nicht mit einem Dialogfeld aufgelöst werden konnte, oder weil das MAPI_DIALOG-Flag nicht festgelegt wurde, gibt **ResolveName** MAPI_E_AMBIGUOUS_RECIP. Wenn einige der Empfänger mehrdeutig sind und einige nicht aufgelöst werden können, kann **ResolveName** einen der Fehlerwerte zurückgeben. 
  
Wenn ein Name nicht aufgelöst werden kann, kann der Client eine eindeutige Adresse mit einer speziell formatierten Adresse und einem Eintragsbezeichner erstellen. Weitere Informationen zum Format von one-off-Eintragsbezeichnern finden Sie unter [One-Off Entry Identifiers](one-off-entry-identifiers.md). Weitere Informationen zum Format von einmal verwendeten Adressen finden Sie unter [One-Off Addresses](one-off-addresses.md).
  
MAPI unterstützt Unicode-Zeichenzeichenfolgen für **die ADRLIST** und die neuen Eintragstitelparameter zu **ResolveName**; Wenn Sie das MAPI_UNICODE festlegen, werden die folgenden Eigenschaften als Typ zurückgegeben, PT_UNICODE in den [ADRENTRY-Strukturen](adrentry.md) verwendet werden: 
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Die eigenschaft **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) wird jedoch immer als Typ PT_STRING8.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI verwendet die **ResolveName-Methode,** um eine einmal festgelegte Adresse zu lösen, bevor sie einer Nachricht hinzugefügt wird.  <br/> |
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI verwendet die **ResolveName-Methode,** um einen Adressbucheintrag nach Anzeigenamen zu suchen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

